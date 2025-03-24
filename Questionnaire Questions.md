# Android Upgrade Series Questionnaire Investigation

**Background:** Mobile vendors develop their customized Android versionsbased on the Android Open Source Project (AOSP) led byGoogle. As the AOSP releases new versions frequently, vendors need to periodically carry out the Android upgrade. Both the AOSP and Android variants independently undergo extensive and complex modifications. Consequently, Android upgrades often lead to compatibility issues and conflicts. To systematically define, study, and resolve these conflicts during the Android upgrade process, we kindly request you to dedicate 15 minutes to complete the following survey. Your participation will greatly assist us in gathering insights. This survey will be anonymized, focusing solely on trends and improvement suggestions.



1. Which features or modules are you primarily responsible for developing? [Open-ended Question]

   

2. How many versions have you participated in conflict resolution for system upgrades? [Single-select Question]

   - < 5 times  
   - 5 - 10 times  
   - 10 - 50 times  
   - &gt; 50 times

3. How many years of Android work experience do you have? [Single-select Question]

   - < 1 years
   - 1 - 5 years
   - 5 - 10 years
   - &gt; 10 years

4. How many conflicts have you resolved in total? [Single-select Question]

   - < 10 conflicts
   - 10 - 100 conflicts
   - 100 -1000 conflicts
   - &gt; 1000 conflicts

5. What types of conflicts have you resolved during the conflict resolution process? [Multiple-answer Question]

   - Method block conflicts
   - Class member variable conflicts
   - Import conflicts
   - Interface parameter conflicts
   - Scope changes of method blocks or class member variables (e.g., public to private)
   - Changes in inherited native methods
   - Final modifier restrictions
   - Annotation changes
   - Inner class modifications
   - AOSP code updates
   - Renaming conflicts
   - Comment conflicts
   - Interface changes
   - Indirect conflicts

6. How many steps does your process for resolving a single conflict in codex involve? (Your understanding of conflicts is important for tool development and training) [Open-ended Question]

   

7. Which conflict resolution methods do you use more frequently? [Multiple-answer Question]

   - Keep upstream  
   - Keep downstream  
   - Merge upstream and downstream

8. Does the conflict resolution process involve code or files outside the conflict blocks? [Single-select Question]

   - None  
   - Involves other code within the conflict file  
   - Involves 1-2 files  
   - Involves multiple files

9. How do you handle conflict code that repeatedly appears in multiple versions? [Multiple-answer Question]

   - No repeated conflicts found  
   - Directly refer to previous merging methods  
   - Analyze and merge each time individually  
   - Choose based on the similarity to previous cases

10. Based on your experience, what do you think are the causes of conflicts? [Open-ended Question]

    

11. What is the total time allocated for your conflict resolution tasks? [Single-select Question]

    - 1 day
    - 5 days
    - 7 days
    - Although ample time is given, it is always done at the last moment.

12. How many steps does your process for resolving a single conflict involve? What is the time distribution for each step? [Open-ended Question]

    

13. How long does it typically take to resolve a complex conflict? Does it require assistance from other engineers, such as voice models or conflict change commits? [Open-ended Question]

    

14. How often do you review Google commits and self-developed commits when analyzing the causes of conflicts? [Single-select Question]

    - Never  
    - Occasionally  
    - Frequently

15. What technical challenges do you usually encounter when resolving merge conflicts? [Open-ended Question]

    

16. Which specific types of conflicts are more difficult to handle? [Multiple-answer Question]

    - Method block conflicts
    - Class member variable conflicts
    - Import conflicts
    - Interface parameter conflicts
    - Scope changes of method blocks or class member variables (e.g., public to private)
    - Changes in inherited native methods
    - Final modifier restrictions
    - Annotation changes
    - Inner class modifications
    - AOSP code updates
    - Renaming conflicts
    - Comment conflicts
    - Interface changes
    - Indirect conflicts

17. Resolving conflicts requires understanding Google's historical solutions. Please assess your familiarity with these solutions on a scale of 1-10. (1 - Least familiar, each solution needs to be understood from the basic architectural principles; 6 - Need to individually review commits and understand historical solutions; 10 - Very familiar, no need to review commits, and already know the solution) [Single-select Question]

    

18. Resolving conflicts requires understanding self-developed project historical solutions. Please assess your familiarity with these solutions on a scale of 1-10. (1 - Least familiar, each solution needs to be understood from the basic architectural principles; 6 - Need to individually review commits and understand historical solutions; 10 - Very familiar, no need to review commits, and already know the solution) [Single-select Question]

    

19. Resolving conflicts requires understanding Google's new upgrade solutions. Please assess your familiarity with these solutions on a scale of 1-10. (1 - Least familiar, each solution needs to be understood from the basic architectural principles; 6 - Need to individually review commits and understand historical solutions; 10 - Very familiar, thorough initial commit analysis, can quickly recall issues) [Single-select Question]

    

20. Would you be willing to accept a follow-up interview? (We can discuss the evolution of upgrades together, making future upgrades smoother) [Single-select Question]

    

21. What tools or resources do you typically use when handling conflicts? [Open-ended Question]

    

22. Have these tools effectively helped you reduce conflict resolution time or improve efficiency? [Open-ended Question]

    

23. During the conflict resolution process, which team members (e.g., other developers, testers, project managers) do you usually need to collaborate with? [Open-ended Question]

    

24. Is the collaboration effective, and is there room for improvement? [Open-ended Question]

    

25. What kind of emotional pressure do you usually feel during the conflict resolution process? [Open-ended Question]

    

26. Are there any specific supports or strategies that help you cope with project-related stress? [Open-ended Question]

    

27. Based on your experience, what methods or tools do you think could improve the current conflict resolution process? [Open-ended Question]

    

28. When using existing tools, what issues do you think still need improvement or optimization? [Open-ended Question]

    

29. What suggestions do you have for new developers to help them resolve such issues more effectively? [Open-ended Question]

    

30. Can you share an experience of particularly difficult or successful conflict resolution? [Open-ended Question]

    

31. What important lessons have you learned from these experiences? [Open-ended Question]

    

