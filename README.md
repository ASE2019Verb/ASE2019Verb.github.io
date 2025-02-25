#### Replication package for paper: Detecting Inconsistent API Functionality Descriptions in Reference Documentation and Developer Questions

##### Attention:

We call the functionality sentence  _f\_sentence_

A  _f\_sentence_ can be classiﬁed into a functionality category (or _f\_category_)

The _f\_sentence_ from a _f\_category_ share a set of phrase patterns (or _p\_pattern_)

##### RQ1: What verbs are used in the API _f\_sentences_

1. [sorted_verb_count.txt](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ1/sorted_verb_count.txt) shows the all verbs we collect from _f\_sentences_ of Java and Android API methods. There are 931 verbs including the verb "return", and 87 verbs(9.34%) of them appear in 80% _f\_sentences_. 930 verbs excluding the verb "return", and 115 verbs(12.37%) of them appear in 80% _f\_sentences_.
2. [verb_count.xlsx](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ1/verb_count.xlsx) includes the appearance count in _f\_sentences_ of all 931 verbs. Each row contains four parts. The first part is the verb, the second is the appearance count of this verb, the third is the index, and the last part is the log result of the count. Also, there are four figures that show the trend of the verb count's change. 
3. Total _f\_sentences_ (54256). [total_functionality_descriptions.csv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ1/total_functionality_descriptions.csv) contains 54,256 _f\_sentences_ filtered from Java and Android API methods. Each piece of data contains API's qualified name and its _f\_sentence_.

##### RQ2: What _f\_categories_ can the _f\_sentences_ be classified into?

1. [functionality_category.tsv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ2/functionality_category.tsv) shows the _f\_categories_ we summarized. It mainly includes four parts. The first column shows the total verbs of each _f\_category_, the second column is the label verb of each _f\_category_, the third is the number of verbs that each _f\_category_ contains and the last column shows three example _f\_sentences_ of each _f\_category_.

   For example, the label verb of functionality category "cancel/deregister/undo/deny/unset/unschedule/unregister/unbind/uninitialize/unload/deselect/unlock/unblock" is "cancel", it contains 13 verbs. ['Cancels the speech recognition.', 'Instructs the WebView to cancel the authentication request.', 'Cancels the current editing session.'] are three example _f\_sentences_ of this category.

2. [annotation_website](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ2/annotation_website.png) is a screenshot of our annotation website.

##### RQ3: What _p\_patterns_ are used in the _f\_sentences_ from each _f\_category_?

1. [functionality_category_sentence_pattern.json](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ3/functionality_category_sentence_pattern.json) shows all _p\_patterns_ used in the _f\_sentences_ of each _f\_category_ and the count of each _p\_pattern_ in each _f\_category_.

2. [pattern_count.xls](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ3/pattern_count.xls) contains two parts. The first part is the number of _p\_patterns_ for each _f\_category_ and the second part is the count of _p\_patterns_ for n-ary _p\_patterns_.

   The first part includes three columns. The first column is the index of each _f\_category_, the second column is the number of _p\_patterns_ that each _f\_category_ used and the last column is the total verbs of each _f\_category_.

   The second part mainly includes a figure which can shows the numbers clearly.

3. [first_80\_pattern_count.xls](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ3/first_80_pattern_count.xls) shows the number of _p\_patterns_ for each _f\_category_ and the number of _p\_patterns_ that appear in 80%  _f\_sentences_. It mainly includes two parts. The left is the data of the number of _p\_patterns_ for each _f\_category_ and the number of _p\_patterns_ that appear in 80%  _f\_sentences_ sorted by the number of _p\_patterns_, the right is a figure that describes this trend.

##### RQ4: What is the impact of the inconsistencies between API _f\_sentences_ and developer queries on API retrieval?

1. [questions.tsv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ4/questions.tsv) shows the annotation results of the questions by two annotators. It contains 13 columns. The first column is the raw question, the second is the final _p\_pattern_ of the question and the third is the raw verb of the question. Column 4 - 7 are the annotation results by the first annotator which include the revised _f\_sentence_, the revised verb, the index of _f\_category_, the value whether it is a _f\_sentence_. Column 8 - 10 are the annotation results by the second annotator. Column 11 and 12 are the final results of the annotation, and the last column is the index.
2. [api_descriptions.tsv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ4/api_descriptions.tsv) has the similar structure to [questions.tsv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ4/questions.tsv). It mainly includes 14 columns. The first column is the index, the second is the qualified name of API method, the third is the raw _f\_sentence_ of each API method. Column 4 - 5 show the final annotation results of each _f\_sentence_. Column 6 is the value whether these two annotators are consensus. Column 7 is the raw verb, column 8 is the revised verb, column 9 is the index of the _f\_category_ that teh revised verb belongs to and column 10 is whether the API description is a  _f\_sentence_. Column 11 and column 13 are the annotation results by the first annotator which include the revised verb and revised _f\_sentence_. Column 12 and column 14 are the annotation results by the second annotator.
3. [MRR_results_before_revising_by_lucene.csv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ4/MRR_results_before_revising_by_lucene.csv) and [MRR_results_after_revising_by_lucene.csv](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/RQ4/MRR_results_after_revising_by_lucene.csv) are the results evaluated by Lucene. They both contain three columns. The first is the index, the second is the rank of the result and the third is the rec. rank of the result.

##### Application:

1. [Biker_data_results](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/Biker_data_results) includes four parts. [description_prediction_results](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/Biker_data_results/description_prediction_results) and [question_prediction_results](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/Biker_data_results/question_prediction_results) are the results by our application and the other two parts [description_annotated_results](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/Biker_data_results/description_annotated_results) [question_annotated_results](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/Biker_data_results/question_annotated_results)are the annotated results. Each part contains four dataset files. Type0 represents the data that are not inconsistent, type1 represents the data that are unknown, type2 represents the data that belong to the verb inconsistency and type3 represents the data that belong to the _p\_pattern_ inconsistency.
2. [POI_Result](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/POI_Result) contains the annotation results by the six annotators. [poi_results.txt](https://github.com/ASE2019Verb/ASE2019Verb.github.io/blob/master/Application/POI_Result/poi_result.txt) shows the average score of each annotator and the total average score of the results.