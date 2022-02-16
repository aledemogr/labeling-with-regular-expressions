# labeling-with-regular-expressions
AKA how start getting around using grep, grepl, sub, gsub, regexp, gregexp.

Main difference between them is that while grep and grepl matches to pattern within the character vector, regexpr and gregexpr return more detail. sub and gsub perform replacement on the basis of a regular expression.

This is my version of lazy labeling: run the same code changing just the input dataset

file <- "BEN_Benin_2013" #myfile
clabel <- substring(file, 1, 3) #country label is the iso3 code
cname <-sub( ".*_(.*)_.*", "\\1", file) #country name
year <- sub( ".*_(.*)_*", "\\1", file) #census year
