# Set the working directory (location)
setwd("C:/Users/Steven/Desktop") # Be aware of the direction of slashes

# Get the working directory
getwd()

# Read csv file
apoe <- read.csv("POCD.csv")

# Read csv file without setting the working directory: (location+file name)
apoe <- read.csv("C:/Users/Steven/Desktop/POCD.csv")

# Saving data into R Data Format
save(apoe, file = "apoe.RData")

# Reading a R dataset
load("apoe.RData")


# Call package
library(meta)

# metabin => Four variables
apoe.iv<- metabin(tcases,ttotal,ccases,ctotal,studlab=trialnam,method="I",sm="OR",data=apoe)
apoe.iv
forest(apoe.iv)

# subgroup analysis (byvar=the subgroup)
apoe.sub <- metabin(tcases,ttotal,ccases,ctotal, studlab=trialnam, sm="OR", data=apoe, byvar=surgery)
forest(apoe.sub)


# Call package
library(metafor)
dat <- apoe

### calculate log odds ratios and corresponding sampling variances
dat <- escalc(measure="OR", ai=tcases, bi=tnoncases, ci=ccases, di=cnoncases, data=apoe)

### fit random-effects model
res <- rma(yi, vi, data=dat)

### contour-enhanced funnel plot
funnel(res, yaxis = "seinv", level=c(90, 95, 99), shade=c("white", "gray55", "gray75"))

### calculate log odds ratios and corresponding sampling variances
dat <- escalc(measure="OR", ai=tcases, n1i=ttotal, ci=ccases, n2i=ctotal, data=dat, subset=-16)

### fit random-effects model
res <- rma(yi, vi, data=dat)
res

### classical Egger test
reg <- regtest(res, model="lm")
reg
se <- seq(0,1.8,length=100)
lines(coef(reg$fit)[1] + coef(reg$fit)[2]*se, se, lwd=3)
