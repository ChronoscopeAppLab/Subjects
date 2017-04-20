# List of subjects for Liftim

List of subjects for Liftim is defining subject theme color, written in [JSON](http://json.org/).
Main data exists under `presetSubjects` directory. Users can choose suitable subjects preset because we have variety of subject definition file for a variety of type of class. If you contribute this repository, supported types of classes will be increased.

## To add subject definition file
Theme colors are being defined using [Color palette](https://material.io/guidelines/style/color.html#color-color-palette) of Matrial design guidelines.

Before contribute this repository, please look at following code and list to understand our coding style and meaning of key and value.
```
[
  {
    "subject": "国語",
    "shortSubject": "国語",
    "color": "red"
  },
  {
    "subject": "現代社会",
    "shortSubject": "現社",
    "color": "yellow-800"
  }
]

```
(Currently we support only Janpanese but someone translate, we would like to the other languages)

Key | Discription | Type
---- | ---- | ----
`subject` | Formal subject name | `String`
`shortSubject` | Informal, short subject name | `String`
`color` | Subject theme color | `String`

Order of keys doesn't have any affects for parsing data but look at code around you and make effort to write uniformed code.
If you define a color not defined at the palette, Liftim will handle as an undefined color and display hardcorded color(e.g. gray).

## How to use GIT command?
If you don't know how to use git command, you can contribute following step-by-step guide. Git is available [here](https://git-scm.com/).
(If you aren't in the Chronoscope organization, please fork this repo at first)

###### 1.clone repository
```
cd /tekitouna/directory/
git clone https://github.com/ChronoscopeAppLab/Subjects.git
```

###### 2.make branch
```
git branch BRANCH-NAME
```

###### 3.checkout branch you made
```
git checkout BRANCH-NAME
```

###### 4.edit file

###### 5.commit changes
```
git add --all
git commit -m "COMMIT-MESSAGE"
```

###### 6.push
```
git push origin BRANCH-NAME
```

###### 7.open pull request on GitHub
Open GitHub and click OpenPullRequest button to open pull request.
