# PI4 Computational Bootcamp 2017

This repository contains the syllabus and materials for the 2017 PI4 bootcamp. 

It is a website generated by the R blogdown package.

## How to use

### EZ post a new lesson

* put a markdown file in lessons/

### Advanced 

#### Install blogdown package

* open R studio
* install `blogdown` package

```r
# works with R <= 3.3
install.packages('blogdown') 

# if using R 3.4
install.packages('devtools')
devtools::install_github("rstudio/blogdown")
```

#### Update information

* homepage in `content/_index.md`
* syllabus in `content/syllabus.md`.

#### Post a new lesson

```r
blogdown::new_post()
```


#### build site

```r
blogdown::build_site()
```

### Commit and push 

Check in all .md, .Rmd, and .html files.

## Dependencies

Because the dependencies are complex, most of the tutorials are written in environments hosted at terraref.ndslabs.org. There students are able to launch web-based programming environments with all of the dependencies already available. [This article](http://www.nationaldataservice.org/news/170329_workbench.html) describes this tool, which is really amazing as it is incredibly difficult to setup identical environments for students. With many connections to remote computers this becomes even more challenging. And previously, there was no way to provide students with easy access to a very large filesystem and a friendly programming environment.

### Data

* Many online databases (especially betydb.org) will be used via both the web front end and the 
* Data on the ROGER supercomputer is mounted to the terraref.ndslabs.org database in the `/data` directory
* 
### Shell Lessons

### SQL Lessons

A connection to the TERRA REF trait database

```
ssh -Nf -L 5432:localhost:5432 bety6.ncsa.illinois.edu
```

### R Lessons

For R material we are using docker images defined in the [terraref/toolserver-dockerfiles](https://github.com/terraref/toolserver-dockerfiles) GitHub repository. 

Handy additions:

```r
install.packages('addinlist')
```