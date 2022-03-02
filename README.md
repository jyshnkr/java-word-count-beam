# Java-word-count-beam - JAYASHANKAR MANGINA

### Instructions to run the Java word-Count:

0. Navigate to your 44517 directory and open with Powershell (as Admin)

1. Download and install the [Java Development Kit (JDK) version 8](https://www.oracle.com/java/technologies/downloads/). Verify that the JAVA_HOME environment variable is set and points to your JDK installation.

2. Download and install [Apache Maven](https://maven.apache.org/download.cgi) by following [Maven’s installation guide](https://maven.apache.org/install.html) for your specific operating system.

3. Use the following command to generate a Maven project that contains Beam’s WordCount examples in your directory.

> mvn archetype:generate `
 -D archetypeGroupId=org.apache.beam `
 -D archetypeArtifactId=beam-sdks-java-maven-archetypes-examples `
 -D archetypeVersion=2.36.0 `
 -D groupId=org.example `
 -D artifactId=word-count-beam `
 -D version="0.1" `
 -D package=org.apache.beam.examples `
 -D interactiveMode=false
 

4. This will create a word-count-beam directory that contains ```a pom.xml```

5. Now, navigate to word-count-beam directory

> ```cd .\word-count-beam```

6. Following command will list out the contents in the word-count-beam directory

> ```dir```

7. Navigate to the examples folder by typing below command in your powershell

> ```dir .\src\main\java\org\apache\beam\examples```

8. Create a empty text file and copy the contents from this [link](https://00f74ba44b963764a31d794cfbb9a16a8904a8d4a9-apidata.googleusercontent.com/download/storage/v1/b/apache-beam-samples/o/shakespeare%2Fsonnets.txt?jk=AFshE3UR-5dRvKFmq7toNMefNLl9aaKaOZ3bwuzGskJB6MLNBOcWO9eE4wSQL1mcmUrXTt7N2XqgPFgiJPJKwXAB584AQsanNLk5plxmhohU7Oro4AlUCeV5RvvEG1-dSmnvRuoLaLC1noKFygH0RiI_ZSNZdiSGaoZPOSLTvgDbSA6p15pAgRm4mXZFoXySSqDC7QSqYIdUEkqbOMlMLhNTejjWSszS_aMIbzlotAfS7f9MG0wTj8EmJdzITx3y8CKejID_u4T-6FgXWZNcz41ggCrWrudkYlnV5tf_tuz1fiWygYIPz3X7RHgvTYajzFNy_6P2LBGB5anPkBoMZy6XGeG7yboZ0ogCAkSlfqyvLRAvOjM598g4xi4R-LDxc5XMsO-CHkNQwBPjyiI4vVKCT9PrJj2Y0IjbqarKJGy4TjboRxRKw-9E7kXUj6c609PSMtrnPrM5ASDJBYcdBfUgGfgLI9f1esDTdp-TyDo2RPt7wfx86bYkLlqwqiEEeh4LKOeQ-87c6qowMXeltZzA2lKJvROcgK8_8IpGYfS44IxFfRh1loFZZAK5bbOA7JJYtGMyEou0jPPIZzQs-sIBgYVSsfvsTv-wHvuJ1pwGE5lDk7NSf69m0HoQYmKFOQQUpaZYtak_lXR2zAa3fmt8ANLnUSFMgT_27mjkLzd6uJMB-_DE1leP-glg3GUkiIXIY5J1bGHTNiq2XjqBUR9Satr1fgMfmVw2Zlu2tLZjFGBrD-FcK75qMJ4xGqOeXuUOO8QudDQSMw3q6HcKWRUCwhajOIrweZkbet8bn2yrsspixoOY71wqlzrDRuo64QkvXFOyahkoNkWG5sNrtgmrfUH8uZ2UkdrYzZGaBMK_cxOrFvtcf-5w5roCNkM01eya0M1t_P_kNI_QmuhXjaXecjq2pm0l9rVMb-ICZ18CoIj5h8JC19Qlw-YNxla_OrpfKgrz3UimYLgVV7ncCg-nj3Ont6I&isca=1). Paste it in your text file.

9. Now, execute the pipeline in Powershell.

> mvn compile exec:java -D exec.mainClass=org.apache.beam.examples.WordCount `
 -D exec.args="--inputFile=sample.txt --output=counts" -P direct-runner

10. You can find the output file in your directory. Open with VS Code to view the counts output file.


