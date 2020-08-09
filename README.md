# Final-S-E-assignment

paper 1

    SUMMERY 
   TOPIC:

Using Large-Scale Anomaly Detection on Code to Improve
Kotlin Compiler
  AUTHORS NAME:

Timofey Bryksin, Victor Petukhov, Ilya Alexin, Stanislav Prikhodko, Alexey
Shpilman, Vladimir Kovalenko, and Nikita Povarov. 2020.
 
CONFERENCE NAME: Mining Software Repositories (MSR'20),

Using LargeScale Anomaly Detection on Code to Improve Kotlin Compiler. In 17th
International Conference on Mining Software Repositories (MSR ’20), October
5–6, 2020, Seoul, Republic of Korea. ACM, New York, NY, USA, 11 pages.

                       INTRODUCTION:

In software engineering,anomaly techniques have been successfully applied to a variety of practical tasks in many areas. 
These techniques help to detect cyberattacks,identify pathologies in medical images and detect traces of fraudulent activities in financial data.       
In Software engineering, anomaly detection is widely applied to findind bugs, security issues, workflow errors and other anomalous patterns in code or others software artifacts.
we propose a new area of application for anomaly detection, finding issues in programming language compilers.
we define a code that are not typical wittin the community or an ecosystem of a giving programming language or machine code that is uncharacteristic within the range of output produced by the compiler.
such code should be useful to both users and developers of the language.  
Established industry of standard languages such as Java and C++ are not the more feasible targets for detecting  anomiles at the scale of a language ecosystem. 
while large amounts of open source codein these languages are publicly available, mainstream compilers are very well-tested and stable, which makes it hard to identify unknown compiler issues through anomaly detection.
we choose kotline and its ecosystem as a target for this study. 
Since the language is relatively young, its compiler might still contain bugs and performance issues.
The paper is all about threefold:
.A method for finding code anomalies
.A set of tools implementing the proposed method and as well as more than four million unique kotline functions collected from GitHub and the bytecode.
. The evalution of the proposed method on the collected dataset.

                 RESEARCH METHODOLOGY:

The GrouMiner tool was developed to detect anomalous patterns in object interaction in java programs.
The tool performs a static code analysis.
Contextual anomalies occur when a single data object is anomalous in a specific context but not otherwise.
Collective anomalies occur when linked objects are observed against other objects as an anomaly.
Syntax trees encoding the latent vector of a nuetral network autoencoder and other distributed code representation.
We perform a search for code anomalies in kotlin programs that are written specifically for the JVM, since it comprises the majority of code written in kotlin.
Our goal is to detect two types of anomiles: syntax tree anomalies and compiler-induced anomalies.
A compiler-induced anomaly is a code fragment that is not an anomaly in the syntax tree form but is an anomaly in the bytecode or vice versa.
We choose to call them compiler-induced because their anomalous nature is revealed only after their bytecode is obtained and analyzed.
To collect a large dataset, we cloned GitHubrepositories that were created before March 2018,stated Kotlin as their main language, and were not forks of some other projects.
We use software metrics and N-grams extraction to embed the syntax tree representation of the code
Software metrics are divided into 4 groups:
• general code metrics: the number of lines of code, the number
of nodes and the height of the syntax tree, etc.
• structural metrics: nesting depth, cyclomatic complexity,
number of branches in “when” expression, etc.
• external metrics of Kotlin functions: the formal arguments
number, type parameters, annotations, the presence of a
suspend modifier, etc.
• the number of particular language elements: expressions,
operators, keywords, function calls, string patterns, etc.
To assess the viability of our approach to identification of anomalies,we conduct an evaluation of significance and practical value of anomalies extracted from the dataset.

                       RESULT:

In this summary i detect two kinds of experiments to different types of code anomalies (syntax tree anomalies and compilerinduced anomalies), using different approaches both at the code
vectorization and at the anomaly detection stages.As a result, 91
syntax tree anomalies and 54 compiler-induced anomalies were
presented for assessment of importance to the Kotlin compiler developers. According to the results of the assessment, 38 syntax tree
anomalies and 31 compiler-induced anomalies were considereduseful (they got rank values 4 and 5). Some of these anomalies were
added into the compiler testing infrastructure as performance and
correctness tests for the compiler front-end and back-end; several
anomalies were postponed for further discussion on possible language design issues. Based on these results and further discussions
with the Kotlin compiler developers, we believe that the detected anomalies are useful and valuable for the language development,and our proposed approach proved itself successful in detection ofvarious code anomalies. 

paper 2

           SUMMARY
 TOPIC:

Characterizing and Identifying Composite Refactorings:
Concepts, Heuristics and Patterns

 AUTHORS NAME:

Leonardo Sousa, Diego Cedrim, Alessandro Garcia, Willian Oizumi, Ana C.
Bibiano, Daniel Oliveira, Miryung Kim, and Anderson Oliveira. 2020. Characterizing and Identifying Composite Refactorings: Concepts, Heuristicsand Patterns. 

 CONFERENCE NAME: Mining Software Repositories (MSR'20),

 17th International Conference on Mining Software Repositories (MSR ’20), October 5–6, 2020, Seoul, Republic of Korea. ACM, New York,NY,USA,12 Pages.

          INTRODUCTION:

Software refactoring is a widely used technique in practice [8, 10,13, 19, 20, 33, 52]. Refactoring consists of a program transformation used to improve software structure, such as removing code smells.
However, from 40% to 60% of the times, developers apply more than one refactoring in conjunction [6, 33], even for removing simple code smells,such as Long Methods.
Recent studies (e.g., [6, 8, 44, 53]) have analyzed a single category
of composite at a time. For example, Palomba et al. [44] and Tufano
et al. [53] analyze temporally-related composites, while Bibiano et
al. [6] and Brito et al. [8] explore spatial composites.
To investigate composite refactorings, we mined the commit
history of 48 GitHub software projects (i) to identify the characteristics of different categories of composite refactorings, and (ii) their effect on either removing or introducing smells.
We observe that nearly 41% of composites are complex, i.e., are
comprised by 3 to 20 interrelated refactorings, which contradicts
a recent finding.
 
                  RESEARCH METHODOLOGY:

 This framework to provide a foundation for our heuristics and our empirical study. Other researchers can also use it to conduct studies based on unambiguous concepts.
A developer can start a composite in
a commit and finish it in the same commit or in the subsequent
commits. In this sense,composite timespan indicates if the composite
is either single-commit or cross-commit.
A heuristic that synthesizes composites
using as scope an individual code element, i.e., either a method
or a class. The goal of this heuristic is to investigate how composites affect an specific element.
In this heuristic, the composite scope is determined by the element used to synthesize the composites.
The commit-based composite heuristic synthesizes as a composite all refactorings performed within a commit.
The range-based composite heuristic considers the notion of refactoring scope to synthesize composites.
In this heuristic, the scope of all refactorings form the composite scope.
we proposed heuristics to identify composites. These heuristics allow one to analyze composites from different, albeit complementary, perspectives. To propose them,we formally defined concepts that characterize a composite.
First, we need to identify the elements affected by each category of composite, but taking into consideration their composite scope.
Then, we analyze what happened with the smells before and after developers apply the composites. To support this analysis, we classify each composite according to their effect on the incidence of smells.
A creational pattern represents a recurring case where the
composite tends to introduce a code smell. A removal pattern
represents a recurring case where the composite tends to remove
a smell. There is no empirical study in the literature that reports
composites that typically remove or introduce smells.
we are able to reveal composites used by developers not only to remove, but also to inadvertently introduce smells.

                        RESULT:



Composite refactoring is common in practice, but a wide empirical
knowledge about it is scarce. To tackle this issue, first, we provided a conceptual characterization of composites and defined two
heuristics to identify composites in different categories. Second, we
investigated how composites manifest in practice, and how they
affect the program structure. Our results show that to study composite we need to rely on different heuristics: they are complementary
to each other, but most empirical studies tend to use only a single
heuristic. For example, the identification of the semantically-related
refactorings was only possible using the commit-based and rangebased heuristics together. Similarly, the identification of several
composite-smell patterns were only possible with the range-based
heuristic.


paper 3

           SUMMARY
TOPIC:

 An Empirical Study of Method Chaining in Java

AUTHORS NAME:
Tomoki Nakamaru, Tomomasa Matsunaga, Tetsuro Yamazaki, Soramichi
Akiyama, and Shigeru Chiba. 2020.

 CONFERENCE NAME: 
 Mining Software Repositories (MSR'20),
An Empirical Study of Method Chaining
in Java. In 17th International Conference on Mining Software Repositories
(MSR ’20), October 5–6, 2020, Seoul, Republic of Korea. ACM, New York, NY,
USA, 10 pages.

                INTRODUCTION:

We present, to the best of our knowledge, the first quantitative study on the use of method chaining that is based on a large set of source code in the real world.
We empirically show the increasing use of method chaining in Java, which has been claimed without empirical evidence in preceding studies [20, 21, 26, 33, 34, 42, 43].
We present language features (or API design) that support method chaining but are not supported yet in Java. We statistically estimated how effective each feature/design would be.
Method chaining is promoted as a good practice that improves the readability of source code. By method chaining, redundant temporary variables and code repetitions are eliminated [8]; related method invocations are grouped into a single expression [34, 42];an expression becomes easy to read from left to right as naturallanguage texts [13, 14, 18, 42].
If you do everything in a single statement then that is compact, but it is less readable (harder to follow) most of the times than doing it in multiple statements.

                  RESEARCH METHODOLOGY:

To build our dataset, we collected 2,814 Java repositories on GitHub.
Those repositories are the ones that were listed at least once in the most-starred 1000 Java repositories on GitHub between Nov.
10th, 2019 and Dec. 21st, 2019. We collected them by monitoring the response of the GitHub API1
every day during that period.
Our dataset contains over three million Java files (approximately seven hundred million lines) in total.
The relative number of method chains has increased from 2010 to 2018 in almost all lengths.
 In our analyses, we use only the code that is newer than or in 2010. 2010 is the year in which the number of repositories exceeds 250 and
in which the number of files exceeds 105 for the first time. We adopt this criterion to avoid that the programming styles of a small
number of old repositories overly affect our analysis.
We performed the Kolmogorov-Smirnov (KS) test to see whether the right tail of ???? in 2018 is generated by a power-law distribution,
a well-known heavy-tailed distribution. The test reported 9 for ???????? and 0.937 for ??-value. The ??-value is greater than the commonly used significance level 0.05. These results of the KS test indicate that it is consistent to assume that the observed values for ?? = 9 are generated by a power-law distribution. Although it is interesting
to discover the generation model of such a distribution, we leave it for future work.
To better understand the trends in method chaining, we manually categorized the method chains in 2018 and 2010 by their behaviors.
For this analysis, we divided the set of method chains into three groups by their length: Short, Long, and ExtLong.
We found 140 chains (50% of ExtLong) in testing code. As mentioned above, all the chains in ExtLong are composed to build an object.
Thus, half of the ExtLong chains build objects for testing.
We found 18 chains (6.43%) using StringBuilder
or StringBuffer in java.lang.

                 RESULT:

This summary was presented our empirical study of method chaining in Java. 
Our analysis quantitatively revealed the widespread and increasing trend of method chaining. 
To provide information for future language/library development, we estimated how effective it
would be to introduce language features and API design for method chaining. 
Although our results support the acceptance of method chaining in the real world, user studies need to be carried out to assert the acceptance. 
It is also interesting and beneficial for a better understanding of method chaining to investigate why real-world programmers prefer (or do not prefer) method chaining. 
The issues mentioned in the StackOverflow thread [8] would be helpful to start such an investigation. 
All of those studies are our primary future work.
