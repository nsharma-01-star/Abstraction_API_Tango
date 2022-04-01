# Abstraction_API_Tango

## Note This is a enhancement project as part of the MSR course 2021/22 at UniKo, CS department, SoftLang Team

## Names of team/students Team: Tango 
## Members: 
* Nisha Sharma (nsharma01@uni-koblenz.de) 
* Pavithree shetty (pavithreerai@uni-koblenz.de) 
* Shweta Mishra (smishra@uni-koblenz.de ) 

## Baseline study: 
### Aspect of the enhancement project: How could projects with multiple POM files impact dependency/usage analysis?


### Input data: 
The java code aims at mining git repositories with following criteria
* A repository with 100 stars and 100 commits
* A repository with more than two contributors
* A repository with at least one source directory
* A repository with one POM file

### Output data: 
Collected repositories
* The csv generated can be found in the output folder - https://github.com/nsharma-01-star/Abstraction_API_Tango/tree/main/output

## Findings of enhancements 
### Process delta:
 * RepositoriesPicker modified to exclude repositories with multiple POM files - https://github.com/nsharma-01-star/Abstraction_API_Tango/blob/main/src/main/java/de/uni_koblenz/gorjatschev/applyingapis/RepositoriesPicker.java

### Output delta:
* The code ran for 19 hour(s), 37 mintues(s) and 38 second(s). However, the following csv files were generated
  * Original work found 19000 repositories with at least 100 stars, we found 19980 Java git repositories with at least 100 stars.
  * Original work filtered 4018 repositories with 100 stars, 2 contributors, 100 commits, we found 1596 Java GitHub repositories with at least 100 stars and one POM file.
  *  dependencies.csv - Original work produced 43798 different dependencies out of 3542 repositories, We found 3562 different dependencies out of 1596 repositories.
  *  dependencies_with_mcrTags.csv - We found 196 entries with mcrTags.
  *  repositories_collected.csv - We found 1596 repositories.
  *  repositories_with_dependencies.csv - We found 903 repositories with dependencies.
  *  repositories_with_mcrTags.csv - Original work found 3532 repositories with mcrTags. We found 499 repositories with mcrTags.
  *  dependencies_counted.csv- We found 3561 dependencies.
  *  dependencies_pair_counted.csv - We found 37 pairs.
  *  dependencies_sets_counted.csv -  We found 896 sets.
  *  mcrTags_sets_counted.csv -  We found 258 sets.
  *  repositories_with_dependencies_similarity.csv - We found 16 intersection.
  *  repositories_with_mcrTags_similarity.csv - We found 4766 intersection.
  
* On running dependencies_counter.py on the csv files generated during the data collection replication part, we were able to find the count of one of the four dependency pair mentioned in the original work and 3 new dependency pairs. 

  * The dependency pair count of the original work is shown in the image below
   ![original work](https://github.com/nsharma-01-star/Abstraction_API_Tango/blob/main/output/output_images/original_output.png)
   
  * The replicated result consisting of dependency pair count by our team tango is shown below
   ![replicated_work](https://github.com/nsharma-01-star/Abstraction_API_Tango/blob/main/output/output_images/replication_output_tango.png)
   
  * The enhancement result consisting of dependency pair count by our team tango is shown below
   ![enhancement_work](https://github.com/nsharma-01-star/Abstraction_API_Tango/blob/main/output/output_images/enhancement_output_tango.png)
   
  * The enhancement result consisting of new dependency pair count by our team tango is shown below
   ![enhancement_work_new](https://github.com/nsharma-01-star/Abstraction_API_Tango/blob/main/output/output_images/enhancement_output_tango_new.png)
   
   * when compared to original work, we found different dependency pairs as shown in the above images.
  

### Implementation of enhancement: 
* Hardware requirements: 
  * OS: Windows, Linux or MacOS 
  * Memory: 16 GB RAM recommended 
  * Processor : Core(TM) i7
* Software requirements 
  * Java 11 (Maven project) 
  * Python 3.9.6 (plotly==5.1.0, pyspark==3.1.2)
* Validation
  * One can compare the above mentioned csv files with the original work, one would infer that the work is enhanced by filtering out the repositories with multiple POM files and that results in modified dependency pairs.
* Data
  * The data replication was able to produce the csv files mentioned in the output delta section.
