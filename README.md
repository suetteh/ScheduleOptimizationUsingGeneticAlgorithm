## Optimize University Part-time Programs Scheduling Using Genetic Algorithm

This study attempted to use computational intelligence algorithm to solve a real-world optimisation problem. Specifically, genetic algorithm (GA) was utilized to generate course schedule for three part-time modular programmes offered by the Asia Pacific University. The part-time structure comprises 5 intakes a year and students are required to take only one module in each intake. 
In order to adapt to the requirements given, 7 hard constraints and a soft constraint were applied to the SE and AI programs while 8 hard constraints and a soft constraint for the DSBA program. 
The goal is to keep hard constraint violation at 0 while soft constraint violation to minimal. The implementation of GA is as shown in the [implementation file](https://github.com/suetteh/ScheduleOptimizationUsingGeneticAlgorithm/blob/main/Implementation_HardSoftConstraints.pdf). Two experiemnts were conducted to compare the performance of the combination of tournament selection and single point crossover, as well as Stochastic Universal Sampling selection and two point crossover.

### Challenges:
Multiple hard constraints are required to be solved. Primarily, the schedule should ensure that each existing and new student has a module to take in each intake so that they are able to complete the programme within 2.5 years. However, a module should not run in consecutive intakes. Concurrently, the operational costs to the university should be minimize. Hence, only a maximum of 5 modules to be offered per intake for each programme. A further complication is that certain modules are offered in two or three programmes which means that these shared modules should be offered at the same intake. Lastly, the research methods module must be offered 3 times a year in January, May and October.

### Data Source:
This project utilized real existing student records of the programs in APU with edited student names.

- The attached StuRec files consists of the list of existing students of the respective programs with the list of modules taken.
  
- The  PT Timetable files include the core modules and electives of the respective programs.

### Tools:
This project was completed using python programming language. The library utilized include:

Distributed Evolutionary Algorithms (DEAP)

numpy

pandas

itertools

matplotlib 

### Conclusion:
Genetic ALgorithm can be an effective tool in optimizing schedule. With generation=100, single point crossover, tournament selection acheived better results. The final schedule is as shown the [Result](https://github.com/suetteh/GeneticAlgoOpt/blob/main/Results.pdf) file. No hard constraint was violated while soft constraint violations were maintained at minimal (not more than 1), in which only 1 or 2 modules are offered more than twice in the academic year.

### Possible Improvement:
In this study, GA was able to keep all hard constraint violations at 0. However, the cost spent by the university might be able to further minimize by maintaining each module to be run not more than twice. Grid search or random search can be applied for hyperparameter tuning. Besides that, other algorithm such as Particle Swarm Optimization (PSO) may further improve the outcome. 


