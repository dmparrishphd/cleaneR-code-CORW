Lists
=====

This article is about lists
(\[[1](https://www.lexico.com/en/definition/list)],
\[[2](https://www.merriam-webster.com/dictionary/list)],
\[[3](https://www.wordsmyth.net/?level=3&ent_l=list&rid=24059)]),
which have some things in common with
[`list`](https://cran.r-project.org/doc/manuals/r-release/R-intro.html#Lists)-s,
but are not idential with them.

A List in the Shape of a List
-----------------------------

Choose an easy-to-read list format. Here are some alternatives:

The wide list:

    "tidyverse", "RODBC", "readr", "purrr", "dplyr", "readxl", "xlsx", "tidyr", "ggplot2", "proj4", "sf", "rgdal", "maptools", "plyr", "lubridate", "reshape2", "png", "Cairo", "crayon", "rio", "tictoc", "ggforce"

The wrapped list:

    "tidyverse", "RODBC", "readr", "purrr", "dplyr", "readxl", "xlsx",
    "tidyr", "ggplot2", "proj4", "sf", "rgdal", "maptools", "dplyr",
    "lubridate", "reshape2", "png", "Cairo", "crayon", "rio", "tictoc",
    "ggforce"

The vertical list:

    "tidyverse",
    "RODBC",
    "readr",
    "purrr",
    "dplyr",
    "readxl",
    "xlsx",
    "tidyr",
    "ggplot2",
    "proj4",
    "sf",
    "rgdal",
    "maptools",
    "dplyr",
    "lubridate",
    "reshape2",
    "png",
    "Cairo",
    "crayon",
    "rio",
    "tictoc",
    "ggforce"

A Well Ordered List
-------------------

An alphabetized list may also be an option:

    "Cairo",
    "RODBC",
    "crayon",
    "dplyr",
    "dplyr",
    "ggforce",
    "ggplot2",
    "lubridate",
    "maptools",
    "png",
    "proj4",
    "purrr",
    "readr",
    "readxl",
    "reshape2",
    "rgdal",
    "rio",
    "sf",
    "tictoc",
    "tidyr",
    "tidyverse",
    "xlsx"

A Built List
------------

You can build a list with code, too:

    character.text <- function ( x ) scan (
        what = "" ,
        sep = "\n" ,
        strip.white = TRUE ,
        text = x )
    
    NAMES.PACKAGES <- character.text ( "
    
        Cairo
        RODBC
        crayon
        dplyr
        dplyr
        ggforce
        ggplot2
        lubridate
        maptools
        png
        proj4
        purrr
        readr
        readxl
        reshape2
        rgdal
        rio
        sf
        tictoc
        tidyr
        tidyverse
        xlsx
        
        ")

_Reminder_: you can define `character.text` once and use it over and over.
