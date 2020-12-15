# quebs-cv
A Québecois French ⚜ CV for young academics written in markdown 

## Credits: 
Original code written by Claud D. Park <posquit0.bj@gmail.com>

Downloaded from [Awesome-CV](https://github.com/posquit0/Awesome-CV)

License: [LPPL v1.3c](http://www.latex-project.org/lppl)

## Step one to a Quebs French CV
Create and R project with the .md file, a headshot photo, and the .cls file.

You will need to download the vitae, tinytex, and tibble packages from R. You might also need to download [LaTexiT](https://download.cnet.com/LaTeXiT/3000-2053_4-66890.html)

## Edit the markdown file, here are some cheats
** before and after a word or phrase makes them **bold**

"*" before and after a word or phrase makes them *italicized*

"#" is a level one heading

"##" is a level two heading

"###" is a level 3 heading

"[title](https://www.example.com)" Surrond "title" with square brackets followed by (https://www.example.com) is a link

## Think of WWWWWH
Who, what, when, where, why, and how

All of the entries follow some sort of list of list of these things

### Example: 
These are some awards I won. The criteria in the code include: (**where/who** ~ Org, **what** ~ Title,  **why/how** ~ Desc, **when** ~ Year) refer to the organization, title of the award, the description, and the year it was won. 

````{r}
tribble( ~ Org, ~ Title, ~ Desc, ~ Year, 
"Société Canadienne de Psychologie", "Certificat d’excellence universitaire", "ayant présenté un de les meilleurs travaux (dissertation, maîtrise et thèse) au niveau du baccalauréat à l'Université Concordia", "2019",
"Université Concordia", "Première place (2019), Deuxième place (2018)", "présenter une méthodologie en équipe pour le concours Inter-University Psychology Case Competition", "2018 & 2019",
"Université Concordia", "Liste du doyen", "ayant maintenue une GPA de 3.75 annuelle", "2016-2017, 2018-2019",
"Université Concordia", "Garnet Key Society Merit Award", "une contribution exceptionnelle à la 60e Garnet Key Society", "2018",
"Université Concordia", "Shuffle Entrance Scholarship", "réussite académique exceptionnelle (Bourse de 1000$)", "2016",
"Collège John Abbott", "Islanders Certificate of Academic Achievement", "ayant maintenue une moyenne générale de plus de 80% comme étudiante-athlète", "2016") %>% 
  detailed_entries(
    with=Title, 
    what=glue::glue("Remis(e) pour: {Desc}."), 
    where=Org, 
    when=Year
    )
````

## When you're done
Hit the "knit" button at the top, it looks like a ball of yarn with a knitting needle, the file will save as a pdf in the folder where you made your R project. 

