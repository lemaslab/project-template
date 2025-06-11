############################################################
## 📦 Load Required Packages Quietly
############################################################
suppressMessages({
  if (requireNamespace("knitr", quietly = TRUE)) library(knitr)
  if (requireNamespace("rmarkdown", quietly = TRUE)) library(rmarkdown)
})

############################################################
## 🎨 Configure knitr and R Markdown Options
############################################################
if ("knitr" %in% loadedNamespaces()) {
  opts_chunk$set(
    fig.path = "results/figures/",  # Where to save figure outputs
    echo = TRUE,                    # Show code in output
    warning = FALSE,                # Suppress warnings in output
    message = FALSE,                # Suppress messages in output
    results = "markup"              # Output format for results
  )
  
  opts_knit$set(
    base.dir = normalizePath(getwd()),  # Base directory for output
    root.dir = normalizePath(getwd())   # Root directory for file paths
  )
}

############################################################
## 🗂️ Ensure Required Directories Exist
############################################################
if (!dir.exists("results/figures")) {
  dir.create("results/figures", recursive = TRUE)
}

############################################################
## 🏠 Define Project Root Directory as Global Variable
############################################################
PROJHOME <- normalizePath(getwd())
assign("PROJHOME", PROJHOME, envir = globalenv())
cat("✅ Project home directory is available as PROJHOME\n")

############################################################
## 🔁 Optional: Reload Utility for Project Functions
############################################################
reload <- function() {
  if (file.exists("R/functions.R")) {
    source("R/functions.R")
    cat("🔁 Functions reloaded from R/functions.R\n")
  } else {
    cat("⚠️ No functions file found at R/functions.R\n")
  }
}

############################################################
## ✅ Initialization Complete
############################################################
cat("ℹ️ R environment initialized for this project.\n")
