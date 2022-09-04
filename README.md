# generate-java-project
Generate Java project template based on IntelliJ (Gradle)


## Prerequisite
1. bash
2. macOS environtment (because of `sed` command)
3. some command:
  - `curl`
  - `git`
  - `sed`
  - `awk`


## How to Install
1. Go to any safe directory.
2. Run
    ```sh
    git clone https://github.com/kyuure/generate-java-project.git
    cd generate-java-project/
    chmod +x generate_java_project
    ```
3. Add script as an alias.

    For zsh user
    ```sh
    cat >> ~/.zshrc <<EOL
    export GTF_JAVA_SG="$PWD"
    alias generate_java_project="\$GTF_JAVA_SG/generate_java_project"
    EOL
    ```

    For bash user
    ```sh
    cat >> ~/.bashrc <<EOL
    export GTF_JAVA_SG="$PWD"
    alias generate_java_project="\$GTF_JAVA_SG/generate_java_project"
    EOL
    ```
    
## How to download
1. Go to safe directory.
2. Run
```sh
bash
curl -#L https://github.com/kyuure/generate-java-project/tarball/namespaces \
  | tar xzv --strip-components 1 \
    --exclude={README.md}
chmod +x generate_java_project
exit
```

## How to Run
Run this command from anywhere
```sh
generate_java_project NameOfTheProject "Problem statement."
```
change `NameOfTheProject` and `Problem statement.` to your liking. <br>
p.s: i'm not responsible for any error ☺️.

### File Structure
After run the file, you'll get the structure with:
```
NameOfTheProject/
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
    │   ├── java
    │   │   └── org
    │   │       └── bootcamp
    │   │           └── nameoftheproject
    │   │               └── Template.java
    │   └── resources
    └── test
        ├── java
        │   └── org
        │       └── bootcamp
        │           └── nameoftheproject
        │               └── TemplateTest.java
        └── resources
```
with `nameoftheproject` and `Template` changed to your input.
And the git log already has one commit, that is `initial commit`.


## How to Test
You can add `generate_java_project` in each line with `echo `.
Then run it. You can see what commands will be executed by `generate_java_project` file.


## Contributors
<table>
  <tr>
<td align="center">
  <img src="https://avatars.githubusercontent.com/kyuure" width="75px;" alt="S Qothrunnada" style="border-radius:50%"/>
  <br/>
</td>
<td align="center">
  <img src="https://avatars.githubusercontent.com/mastree" width="75px;" alt="Kamal Shafi" style="border-radius:50%"/>
  <br/>
</td>
<td align="center">
  <img src="https://avatars.githubusercontent.com/andhikayusup" width="75px;" alt="Andhika Yusup Maulana" style="border-radius:50%"/>
  <br/>
</td>
<td align="center">
  <img src="https://avatars.githubusercontent.com/BeRay31" width="75px;" alt="Reyvan Rizky Irsandy" style="border-radius:50%"/>
  <br/>
</td>
<td align="center">
  <img src="https://avatars.githubusercontent.com/margunwa123" width="75px;" alt="Mario Gunawan" style="border-radius:50%"/>
  <br/>
</td>
  </tr>
</table>



## Reference
- [Why do you need to put #!/bin/bash at the beginning of a script file? - Stack Overflow](https://stackoverflow.com/questions/8967902/why-do-you-need-to-put-bin-bash-at-the-beginning-of-a-script-file)
- [How can I pass a command line argument into a shell script? - Unix - Linux Stack Exchange](https://unix.stackexchange.com/questions/31414/how-can-i-pass-a-command-line-argument-into-a-shell-script)
- [How do I use variables in a sed command? - Ask Ubuntu9](https://askubuntu.com/questions/76808/how-do-i-use-variables-in-a-sed-command)
- [Changing the case of a string with awk - Stack Overflow](https://stackoverflow.com/questions/14139672/changing-the-case-of-a-string-with-awk)
