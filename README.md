# generate-java-project
Generate Java project template based on IntelliJ (Gradle)


## Prerequisite
1. bash
2. macOS environtment (because of `sed` command)
3. some command:
  - `curl`
  - `sed`
  - `awk`


## How to Build
1. Go to safe directory.
2. Run
```sh
curl -#L https://github.com/kyuure/generate-java-project/tarball/main \
  | tar xzv --strip-components 1 \
    --exclude={README.md}
chmod +x generate_java_project
```


## How to Run
Just run this command
```sh
./generate_java_project NameOfTheProject "Problem statement."
```
change `NameOfTheProject` and `Problem statement.` to your liking.
p.s: i'm not responsible for any error ☺️.

### File Structure
After run the file, you'll get the structure with:
```
template/
├── README.md
├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
├── settings.gradle
└── src
    ├── main
    │   ├── org
    │   │   └── minibootcamp
    │   │       └── template
    │   │           └── Template.java
    │   └── resources
    └── test
        ├── org
        │   └── minibootcamp
        │       └── template
        │           └── TemplateTest.java
        └── resources
```
with `template` and `Template` changed to your input.
And the git log already has one commit, that is `initial commit`.


## How to Test
You can add `generate_java_project` in each line with `echo `.
Then run it. You can see what commands will be executed by `generate_java_project` file.


## Author
<table>
  <tr>
<td align="center">
  <img src="https://avatars.githubusercontent.com/kyuure" width="100px;" alt="Salsabila Qothrunnada" style="border-radius:50%"/>
  <br/>
  <sub><b>S Qothrunnada</b></sub>
  <br/>
</td>
  </tr>
</table>


## Reference
- [Why do you need to put #!/bin/bash at the beginning of a script file? - Stack Overflow](https://stackoverflow.com/questions/8967902/why-do-you-need-to-put-bin-bash-at-the-beginning-of-a-script-file)
- [How can I pass a command line argument into a shell script? - Unix - Linux Stack Exchange](https://unix.stackexchange.com/questions/31414/how-can-i-pass-a-command-line-argument-into-a-shell-script)
- [How do I use variables in a sed command? - Ask Ubuntu9](https://askubuntu.com/questions/76808/how-do-i-use-variables-in-a-sed-command)
- [Changing the case of a string with awk - Stack Overflow](https://stackoverflow.com/questions/14139672/changing-the-case-of-a-string-with-awk)

