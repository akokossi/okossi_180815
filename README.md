# okossi_180815
JPM Assignment
Objective 0.1


Objective 1:  Data Integrity
JPMCI performs research on data extracted from the production systems of JPMorgan Chase’s lines of business. The primary purpose of these data is to facilitate JPMC serving its customers and clients, not to facilitate economic research. Therefore, after extraction from production systems the data undergo a variety of transformations (including the creation of new calculated fields) before being loaded into our analytical data warehouse. A dominant use case, for example, is de-identification of source data. Since JPMCI uses de-identified data, data owners that sit upstream in the bank must execute de-identification algorithms on source data before it can land in the JPMCI environment. It is on JPMCI to practice good research hygiene by testing data integrity before using the data for economic research.



This objective is designed to provide you with an opportunity to test the research-readiness of a data set.


Objective 1.1: Acquire Source Data
For this exercise, we will use a modified version of the Panel Study of Income Dynamics, produced by the University of Michigan. If you are not already familiar with the PSID, you can review the documentation here: https://psidonline.isr.umich.edu/Guide/default.aspx. The data files have been sent along with this document. Download the data into your Unix-based testing environment, but do not attempt to place them in your repository from Objective 0.1.


Objective 1.2: Test Selection
In general, JPMCI performs the dual role of data creation and data analysis. Since we are using source data, the analogue of which is not generally available to the public, we have no truth set. In this way, there are similarities to organizations like the U.S. Census Bureau. To establish integrity, rather than check against a conceptually identical reference set, we use a battery of tests to gain confidence that the values have not been corrupted upstream of us.
Generate a list of three potential issues that may arise in the collection and transformation of the raw data collected in Objective 1.1 which could feasibly be identified with a data test, and five issues that could not be feasibly identified.  For each of the three that could be identified with testing, provide at least three testing approaches, ordered by those that could be implemented most quickly to those that would take the longest. Note costs and benefits among the options, and choose one test per issue to implement. House this test triage information in a Markdown document, and save it in /obj1/src/. 


Objective 1.3: Validation
Use the three tests identified in Objective 1.2 to probe the files acquired in Objective 1.1 for apparent errors in each field’s data values.  The testing code should be well-structured and documented. The code files should be saved in obj1/code/, and the test results should sit in obj1/out/.


Objective 2: Technical Communication
When engaging in research using data that is administratively collected from within a large firm, no single group owns the entire pipeline. When we have questions or discover issues in our source data, we must communicate our questions/findings to upstream organizational units in an efficient and effective manner. This responsibility is further complicated by the fact that, even within the technical community, people can have different practices and methods of conveying concepts. Providing clear, unambiguous, and actionable information to our partners is difficult to do efficiently and consistently. Consequently, technical communication is critical for our work and a necessary skill for the RSE.


Objective 2.1: Remediation Request
Suppose we have only one partner upstream called Data Owners Anonymous (DOA). DOA’s role is to collect administrative data and de-identify it for our use. (You can speculate about their staffing if it is required for your deliverable.) Your task is to summarize your findings from Objective 1 and recommend a course of action for remediation.  
The summary findings must be clear and readers should be able to consume the main points (as opposed to getting lost in the supporting detail). With respect to proposed remediation, note that you have a limited view of operations performed before the source data landed in the JPMCI environment. As such, you will need to use the limited information you do have to theorize about root causes and appropriate paths forward.  You are free to deliver these findings in either a Markdown document or an HTML slide deck (or some other version-controllable slide format) in the obj2/out/ directory.

