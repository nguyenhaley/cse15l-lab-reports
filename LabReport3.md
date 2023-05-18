# Lab Report 3

## Researching the `grep` command

### Using `-i` with `grep`

**Example 1:**
```
$ grep -i "METHOD" rr74.txt
        Materials and methods
        concentration was determined using the Bradford method
```
When `-i` is used with the `grep` command here, it allows `grep` to search for "METHOD" case-insensitively. This is useful so that any words that are capitalized at the beginning of a sentence will not be overlooked when using `grep`. <br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

**Example 2:**
```
$ grep -i "there" rr74.txt
        levels. We therefore hypothesized that NOS isoforms are
        There was a modest increase in levels of NO metabolites
        endothelium-dependent vasorelaxation, whereas there was an
        NO production despite the increase in NOS expression. There
```
When `-i` is used with the `grep` command here, it allows `grep` to search for a "There" case-insensitively. This is useful so that any words that are capitalized at the beginning of a sentence will not be overlooked when using `grep`. <br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

### Using `-c` with `grep`

**Example 1:**
```
$ grep -c "results" rr74.txt
1
```
When `-c` is used with the `grep` command here, the ouput will be a count of how many lines contained "results." This is useful when you only want to figure out how many lines in a file contain a certain word rather than the lines that contain the word.<br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

**Example 2:**
```
$ grep -c "shown" rr74.txt
5
```
When `-c` is used with the `grep` command here, the ouput will be a count of how many lines contained "shown." This is useful when you only want to figure out how many lines in a file contain a certain word rather than the lines that contain the word.<br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

### Using `-C n` with `grep`

**Example 1:**
```
$ grep -C 2 "decrease" rr74.txt
        pulmonary vasoconstriction. Chronic NOS inhibition did not
        lead to development of pulmonary hypertension [ 3],
        however, possibly because of a decrease in cardiac output.
        These discrepancies have been addressed in recent studies
        using mice that are deficient in NOS isoforms.
--
        physiologic stress that was not seen in more mature animals
        [ 9]. No animals died, however, suggesting that the stress
        was not sufficiently severe to decrease survival during the
        study period. This observation of increased susceptibility
        to hypoxic pulmonary hypertension in younger, developing
--
        piglets 
        in vivo , acute hypoxia caused
        decreased exhaled NO and decreased aortic and pulmonary
        arterial plasma nitrite levels [ 41]. Following chronic
        hypoxia in rats, Sato 
--
        in vitro and 
        in vivo , including impaired arginine
        uptake [ 43], decreased heat shock protein-90 levels [ 44],
        and decreased O 
        2 tension [ 42, 40]. In agreement with
        previous studies, the plasma NO metabolite content in the
--
        circulation as suggested by Toporsian 
        et al. [ 38], then the lack of
        increased NO metabolites could also be due to decreased NOS
        activity in the systemic circulation. However, those
        investigators did not observe any difference in plasma NO
        metabolites in normoxic versus hypoxic rats in which aortic
        NOS was downregulated, but did observe a decrease in
        acetylcholine-stimulated NO release from aortic rings. The
        pattern of NOS expression in vascular beds other than the
```
When using `C n` with `grep` here it prints out out n lines before and after the string "decrease." This is useful because if you are looking for a specific word and want to read more about it, the `C n` command allows you to read the context before and after the word is found.<br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

**Example 2:**
```
$ grep -C 2 "result" rr74.txt
          Nitric oxide metabolites
          To determine whether the increase in NOS in the
          pulmonary circulation following hypoxia resulted in
          increased NO, we measured plasma NO metabolites (Fig. 5).
          There was a modest increase in levels of NO metabolites
--
        expression in systemic and pulmonary endothelial cells from
        different species in cultures [ 31, 32, 33, 34, 35, 36, 37]
        have yielded conflicting results. Recently, Toporsian 
        et al. [ 38] reported 
        in vivo downregulation of eNOS mRNA
```
When using `C n` with `grep` here it allows you to print out out n lines before and after the string "result." This is useful because if you are looking for a specific word and want to read more about it, the `C n` command allows you to read the context before and after the word is found. <br>
*Found on: https://www.geeksforgeeks.org/grep-command-in-unixlinux/*

### Using `-o` with `grep`
**Example 1:**
```
$ grep -o "result" rr74.txt
result
result
```
When using `-o` with `grep` here it only prints out the string "result" rather than all the lines that contain the string "result." This can be useful if you want to extract a specific string out of a file and check to see if you used it too many times. For example, let's say you were writing a report and wanted to see if you used the phrase "therefore" too much. You could use `grep -o` and check how many times the word is returned to gauge whether or not you need to change some words in your report. <br>
*Found on: ChatGPT (a software that is driven by artificial intelligence)*

- **ChatGPT prompt:** "why would  grep -o be useful in linux"
- **ChatGPT output:** <br>

---

The grep command in Linux is used to search for patterns in text files or output from other commands. The -o option is used to print only the matched part of the line, rather than the entire line that contains the match. <br>

Using grep -o can be useful in various situations, such as: <br>
1. Extracting specific information from a large output: For example, if you run a command that produces a lot of output and you only need to extract certain information from it, you can use grep -o to extract only the relevant part. <br>
2. Counting occurrences of a specific pattern: If you want to count the number of times a specific pattern appears in a file or output, you can use grep -o with the wc command to count the number of matches. <br>
3. Manipulating text: If you want to manipulate the output of a command based on a specific pattern, you can use grep -o to extract the relevant part and then use other Linux commands to manipulate the output. <br>

Overall, grep -o can be a powerful tool for working with text in Linux, allowing you to extract and manipulate specific information from files or command output.

---
**Example 2:**
```
$ grep -o "measure" rr74.txt
measure
measure
measure
measure
measure
measure
measure
measure
```
When using `-o` with `grep` here it only prints out the string "measure" rather than all the lines that contain the string "measure." This can be useful if you want to extract a specific string out of a file with the intent to manipulate in some way. For example, let's say you were writing a lab report and you needed to change all of the times you mentioned "measure" to "recorded." Rather than manually search for every time you used "measure," you can utilize `grep -o` to find all of these instances in one go. After this, you can use other commands to help change all of the times you used "measure" to "recorded." <br>
*Found on: ChatGPT (a software that is driven by artificial intelligence)*

---

- **ChatGPT prompt:** "why would  grep -o be useful in linux"
- **ChatGPT output:** <br>

The grep command in Linux is used to search for patterns in text files or output from other commands. The -o option is used to print only the matched part of the line, rather than the entire line that contains the match. <br>

Using grep -o can be useful in various situations, such as: <br>
1. Extracting specific information from a large output: For example, if you run a command that produces a lot of output and you only need to extract certain information from it, you can use grep -o to extract only the relevant part. <br>
2. Counting occurrences of a specific pattern: If you want to count the number of times a specific pattern appears in a file or output, you can use grep -o with the wc command to count the number of matches. <br>
3. Manipulating text: If you want to manipulate the output of a command based on a specific pattern, you can use grep -o to extract the relevant part and then use other Linux commands to manipulate the output. <br>

Overall, grep -o can be a powerful tool for working with text in Linux, allowing you to extract and manipulate specific information from files or command output.

---
