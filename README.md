Download Link: https://assignmentchef.com/product/solved-cmsc-435-assignment-3
<br>
This assignment asks you to develop, evaluate and compare models for the prediction of proteins that interact with nucleic acids using a provided dataset.




<h1>Dataset</h1>

The dataset (<em>dataset_a3.csv</em> file) is provided in the text-based, comma-separated format where each protein is represented by 8 numeric features and 1 symbolic outcome. The outcome feature (called “Class”) annotates each proteins as <em>Yes</em> (interacting with nucleic acids) vs. <em>No</em> (noninteracting). The dataset includes 8795 proteins, with 936 labeled <em>Yes</em> and 7859 labeled <em>No</em>.




<h1>Development of predictive models</h1>

You are required to compute models with version 9.3 (or higher) of the RapidMiner Studio using four different algorithms. Three of these four algorithms must be the Decision Tree, SVM and Naïve Bayes. You can choose any of the other predictive algorithms for the fourth methods. You should parametrize each of these algorithms (select the best possible combination of values of their parameters), to the best of your ability, in order to maximize predictive performance. Note that you will need to read, make an educated guess, and/or use trial-and-error approach to figure out which parameters make a difference and how to use them. <strong>Do not use the “advanced parameters”</strong>. Do not attempt to sample the dataset, i.e., do not perform feature or sample/object selection.




<h1>Evaluation and comparison of predictive models</h1>

You must evaluate the predictive performance using accuracy (“% of correctly classified instances”). For each algorithm you must perform three types of tests:

<ul>

 <li>on the entire dataset (“use training dataset”)</li>

 <li>on 50% of the dataset; you will use the other 50% to compute the model (“percentage split”) – using the 5 fold cross-validation</li>

</ul>

The 5 fold cross-validation divides the dataset at random into 5 equal-size subsets, where one subset is used to test the model and the remaining nine to compute the prediction model. This is repeated 5 times, each time using a different subset as the test set. Consequently, this results in predicting every protein in the dataset. This test type is implemented in the RapidMiner Studio with the “Cross Validation” operator where the number of folds is set to 5.




<h1>Deliverables</h1>

<ol>

 <li><strong>List and briefly describe</strong> the methods that you used (one sentence per method). Provide a <strong>list key parameters</strong> for each method, i.e., parameters that allowed you to improve results when compared with the default parameter values. The key parameters could/should be a subset of all available parameters.</li>

 <li>Using the table shown below, <strong>report the accuracies</strong> for the four algorithms and the three test types. The accuracy values must be reported with two digits after the decimal point, e.g., 91.05. You must include the accuracies of the models that use the default parameters and the</li>

</ol>

best selected parameters. In total, you have 4*3*2 = 24 results to report. <strong>List the best selected values of parameters</strong> for each model and each test type.

<ol start="3">

 <li><strong>Briefly explain</strong> which of the three types of the tests would be appropriate to give the most reliable estimate of predictive performance, i.e., the performance that a user of your model should expect to observe <strong>on new proteins that were not included in the provided dataset</strong>.</li>

 <li><strong>Discuss</strong> whether trying multiple algorithms and adjusting their parameters helped you in developing a more accurate predictive model. If yes then <strong>comment</strong> on whether the corresponding amount of the improvement justifies the amount of effort. Make sure that you rely the <strong>most appropriate test results</strong> (see question 3) when answering this question.</li>

 <li><strong>Discuss</strong> whether the accuracy of your most accurate model is sufficient for practical purposes. <strong>Justify</strong> your answer.</li>

 <li><strong>Give</strong> “confusion matrix” for the most accurate result computed based on the cross validation experiments (selected among the 8 corresponding experiments). Use this matrix to <strong>explain</strong> whether this predictor would be suitable to identify proteins that interact with nucleic acids (Class = <em>Yes</em>), proteins that do not interact with nucleic acids (Class = <em>No</em>), or both types of proteins.</li>

</ol>

<h1><strong>NOTES </strong></h1>

<ul>

 <li>Use a separate, <strong>clearly marked paragraph</strong> for each of the six deliverables.</li>

 <li>The table from the second deliverable must be in the following format; for your convenience this table is provided in the word docx format on the Blackboard. Example values are in green.</li>

</ul>




<table width="618">

 <tbody>

  <tr>

   <td width="147">Reported information</td>

   <td width="112">Test type</td>

   <td width="95">Decision Tree</td>

   <td width="85">SVM</td>

   <td width="95">Naïve Bayes</td>

   <td width="85"></td>

  </tr>

  <tr>

   <td rowspan="3" width="147">Accuracy with default parameters</td>

   <td width="112">Entire dataset</td>

   <td width="95">12.34</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">50%</td>

   <td width="95">23.45</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">Cross-validation</td>

   <td width="95">34.56</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td rowspan="3" width="147">Accuracy with best parameters</td>

   <td width="112">Entire dataset</td>

   <td width="95">45.67</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">50%</td>

   <td width="95">56.78</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">Cross-validation</td>

   <td width="95">67.89</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td colspan="2" width="259">List names of parameters</td>

   <td width="95">maximal depthapply pruning…criterion</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td rowspan="3" width="147">List selected best values of parameters (in the same order as in the list of names)</td>

   <td width="112">Entire dataset </td>

   <td width="95">10True…gain_ratio</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">50% </td>

   <td width="95">13True…gain_ratio</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

  <tr>

   <td width="112">Cross-validation </td>

   <td width="95">-1False…informaton_gain</td>

   <td width="85"></td>

   <td width="95"></td>

   <td width="85"></td>

  </tr>

 </tbody>

</table>


