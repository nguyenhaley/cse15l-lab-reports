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
When using `-o` with `grep` here it only prints out the string "result" rather than all the lines that contain the string "result." This can be useful if you want to extract a specific string out of a file and manipulate in some way. <br>
*Found on: ChatGPT (a software that is driven by artificial intelligence)*

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
When using `-o` with `grep` here it only prints out the string "measure" rather than all the lines that contain the string "measure." This can be useful if you want to extract a specific string out of a file and manipulate in some way. <br>
*Found on: ChatGPT (a software that is driven by artificial intelligence)*
