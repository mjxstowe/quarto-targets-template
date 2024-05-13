source("renv/activate.R")
## For Linux and Windows users, we'll use RStudio Package Manager (RSPM).
if (Sys.info()[['sysname']] %in% c('Linux', 'Windows')) {
	options(repos = c(RSPM = "https://packagemanager.rstudio.com/all/latest"))
	} else {
		## For Mac users, we'll default to installing from CRAN/MRAN instead, since
		## RSPM does not yet support Mac binaries.
		options(repos = c(CRAN = "https://cloud.r-project.org/"))
		# options(renv.config.mran.enabled = TRUE) ## TRUE by default
	}
options(renv.config.repos.override = getOption("repos"))

if (Sys.getenv("INSIDE_DOCKER") == "true") {
  # Docker-specific settings
  Sys.setenv(RENV_PATHS_CACHE = "/renv")
  .libPaths(new = c("/home/rstudio/vscode-R/renv/library/R-4.3/x86_64-pc-linux-gnu", .libPaths()))
}
