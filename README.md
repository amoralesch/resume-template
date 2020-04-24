# Resume Template

This is a skeleton of the current template that I use for my resume.
It builds on top of the example in _TBU_.

It is written in LaTex and uses the following packages:

* [CurVe](https://ctan.org/pkg/curve);
* [silence](https://ctan.org/pkg/silence);
* [ifxetex](https://ctan.org/pkg/ifxetex);
* [ifluatex](https://ctan.org/pkg/ifluatex);
* [graphicx](https://ctan.org/pkg/graphicx);
* [hyperref](https://ctan.org/pkg/hyperref);
* [babel](https://ctan.org/pkg/babel);
* [fontawesome5](https://ctan.org/pkg/fontawesome5);
* [geometry](https://ctan.org/pkg/geometry);
* [relsize](https://ctan.org/pkg/relsize);
* [xcolor](https://ctan.org/pkg/xcolor);
* [pgf](https://ctan.org/pkg/pgf), previously `tikz`;
* _TBU_.

## Make it your own

This repo includes a sample resume, if you want to make it your own,
you need to update the files inside the `rubric` directory. Also have a
look at the `header.tex` and `resume.tex` files.

You can also customize some options (i.e. colors, icons, etc). For this,
check the file `settings.sty`.

### resume.tex

If you have different types of resumes (i.e. full, basic, subject
specific) then create a folder inside `rubric` for each version and
put the rubric files inside it.

Then, modify the line `\newcommand{\cvtype}{XXX}` to select what version
to build.

---

I use CurVe _flavors_ to build resumes in different languages. If you
do the same, update the line `\flavor{XXX}` and use the same value that
you use for suffix in your rubric files.

---

Review the list of rubrics listed inside the document, add as needed.
Please note that if a rubric can be used for any type of resume, it can
be placed directly in `rubric` folder and doesn't need to have the
`\cvtype` value included in the path.

### settings.sty

If using language different than English or Spanish, check the line
`\RequirePackage[main=english, spanish]{babel}` and add as needed.

---

If you want to change the coloes in the doc (icons, lines, headers),
locate the following lines in the file and change the hex values as
needed:

```
\definecolor{HeaderColour}{HTML}{011f4b}
\definecolor{RubricColour}{HTML}{03396c}
\definecolor{SwishLineColour}{HTML}{6497b1}
\definecolor{MarkerColour}{HTML}{005b96}
```

---

If you want to change the icons, find the one you want that is included
in FontAwesome, and then update in the file as follows

| Command            | Current icon     | Used in                                    |
| ------------------ | ---------------- | ------------------------------------------ |
| `geomarker`        | `faMapMarker`    | Icon placed nex to a location.             |
| `prefixmarker`     | `faChevronRight` | Icon to be used for each rubric's entry.   |
| `achievements`     | `faMedal`        | Icon used in the list of achievements.     |
| `responsabilities` | `faCheckDouble`  | Icon used in the list of responsabilities. |
| `tools`            | `faToolbox`      | Icon to be used in the list of tools used. |
