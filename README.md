# rag-bench

RAG-Bench is to summarize all datasets used to evaluate RAG, from document retrieval to question answering. For each dataset, we try our best to accumulate all SOTA results from latest publications, and summarize them into a coherent table. We hope this would help researchers to keep up with the latest deveopments on each benchmark.


## Benchmarks


Here are datasets with the corresponding metrics.

<table>
 <tr>
  <td rowspan=1 align="center"><b>Task</b></td>
  <td colspan=1 align="center"><b>Dataset</b></td>
  <td rowspan=1 align="center"><b>Pubyear</b></td>
  <td rowspan=1 align="center"><b>Documents</b></td>
  <td rowspan=1 align="center"><b>Questions</b></td>
  <td rowspan=1 align="center"><b>Answers</b></td>
  <td colspan=1 align="center"><b>Metrics</b></td>
 </tr>
 <tr>
  <td rowspan=8 align="center">Factoid QA</td>
  <td align="center"><a href="./benchmarks/NQ.md">Natural Questions (NQ)</a></td>
  <td align="center">2019</td>
  <td align="center"><sub>Wikipedia</sub></td>
  <td align="center"><sub>323,045 questions with each an wikipedia page</sub></td>
  <td align="center"><sub>paragraph/span</sub></td>
  <td align="center">Rouge, EM</td>
 </tr>
 <tr>
  <td align="center"><a href="./benchmarks/TriviaQA.md">TriviaQA</a></td>
  <td align="center">2017</td>
  <td align="center"><sub>662,659 evidence documents</sub></td>
  <td align="center"><sub>95,956 QA pairs</sub></td>
  <td align="center"><sub>text string (92.85% wikipedia titles)</sub></td>
  <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/NarrativeQA.md">NarrativeQA (NQA)</a></td>
  <td align="center">2017</td>
  <td align="center"><sub>1,572 stories (books,movie scripts) \& human generated summaries</sub></td>
  <td align="center"><sub>46,765 human generated questions</sub></td>
  <td align="center"><sub>human written, short, averaging 4.73 tokens</sub></td>
   <td align="center">Rouge</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/rajpurkar/squad">SQuAD</a></td>
  <td align="center">2016</td>
  <td align="center"><sub>536 articles</sub></td>
  <td align="center"><sub>107,785 question-answer pairs</sub></td>
  <td align="center"><sub>spans</sub></td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/PopQA.md">PopQA</a></td>
  <td align="center">2023</td>
  <td align="center"><sub>wikipedia</sub></td>
  <td align="center"><sub>14k questions</sub></td>
  <td align="center"><sub>long-tail entites</sub></td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/Rowan/ hellaswag">HellaSwag</a></td>
  <td align="center">2019</td>
  <td align="center"><sub>25k Activity contexts and 45k WikiHow contexts</sub></td>
  <td align="center"><sub>70k examples</sub></td>
  <td align="center"><sub>classification</sub></td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https://allenai. org/data/strategyqa">StrategyQA</a></td>
  <td align="center">2021</td>
  <td align="center"><sub>wikipedia (1,799 Wikipedia terms)</sub></td>
  <td align="center"><sub>2,780 strategy questions</sub></td>
  <td align="center"><sub>its decomposition, evidence paragraphs</sub></td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://allenai. org/data/fermi">Fermi</a></td>
  <td align="center">2021</td>
  <td align="center"><sub>-</sub></td>
  <td align="center"><sub>928 FPs (a question Q, an answer A, supporting facts F, an explanation P)</sub></td>
  <td align="center"><sub>spans</sub></td>
   <td align="center">Accuracy</td>
 </tr>

 <tr>
  <td rowspan=2 align="center">Multi-Hop QA</td>
  <td align="center"><a href="./benchmarks/2WikiMHQA.md">2WikiMultihopQA</a></td>
  <td align="center">2020</td>
  <td align="center"><sub>articles from wikipedia and wikidata</sub></td>
  <td align="center"><sub>192,606 questions each with a context</sub></td>
  <td align="center"><sub>textual spans, sentence-level supporting facts, evidence (tiples)</sub></td>
  <td align="center">F1</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/HotpotQA">HotpotQA</a></td>
  <td align="center">2018</td>
  <td align="center"><sub>The whole wikipedia dump</sub></td>
  <td align="center"><sub>112,779 question-answer pairs</sub></td>
  <td align="center"><sub>text span</sub></td>
   <td align="center">F1</td>
 </tr>
 <tr>
  <td rowspan=4 align="center">Long-Form QA</td>
  <td align="center"><a href="https://huggingface.co/datasets/eli5">ELI5</a></td>
  <td align="center">2019</td>
  <td align="center"><sub>250 billion pages from Common Crawl</sub></td>
  <td align="center"><sub>272K questions</sub></td>
  <td align="center"><sub>multiple sentences</sub></td>
  <td align="center">Citation Recall, Citation Precision, Claim Recall</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/explodinggradients/WikiEval">WikiEval</a></td>
  <td align="center">2023</td>
  <td align="center"><sub>50 wikipedia pages</sub></td>
  <td align="center"><sub>50 questions</sub></td>
  <td align="center"><sub>text spans (sentences)</sub></td>
   <td align="center">Ragas</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/ASQA.md">ASQA</a></td>
  <td align="center">2022</td>
  <td align="center"><sub>wikipedia</sub></td>
  <td align="center"><sub>6,316 ambiguous factoid questions</sub></td>
  <td align="center"><sub>long-form answers</sub></td>
   <td align="center">disambig F1, RougeL, EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/THUDM/webglm-qa">WebGLM-QA</a></td>
  <td align="center">2023</td>
  <td align="center"><sub>-</sub></td>
  <td align="center"><sub>44979 samples</sub></td>
  <td align="center"><sub>sentences</sub></td>
   <td align="center">RougeL, Citation Recall, Citation Precision</td>
 </tr>
 <tr>
   <td rowspan=4 align="center">Multiple Choice QA</td>
   <td align="center"><a href="https://huggingface.co/datasets/truthful_qa">TruthfulQA</a></td>
  <td align="center">2021</td>
  <td align="center"><sub>-</sub></td>
  <td align="center"><sub>817 questions that span 38 categories</sub></td>
  <td align="center"><sub>sentence answer/multiple choice</sub></td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/cais/mmlu">MMLU</a></td>
   <td align="center">2021</td>
   <td align="center"><sub>-</sub></td>
   <td align="center"><sub>15,908 multiple-choice questions</sub></td>
   <td align="center"><sub>4-way multiple choice</sub></td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
  <td align="center"><a href="https://huggingface.co/datasets/allenai/openbookqa">OpenBook QA</a></td>
  <td align="center">2018</td>
  <td align="center"><sub>7326 facts from a book</sub></td>
  <td align="center"><sub>5,957 questions</sub></td>
  <td align="center"><sub>4-way multiple-choice</sub></td>
  <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https://github.com/nyu-mll/quality">QuALITY (QLTY)</a></td>
   <td align="center">2022</td>
   <td align="center"><sub>-</sub></td>
   <td align="center"><sub>6,737 questions</sub></td>
   <td align="center"><sub>4-way multiple choices</sub></td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td rowspan=1 align="center">Open-Domain Summarization</td>
   <td align="center"><a href="https://huggingface.co/datasets/wiki_asp">WikiAsp</a></td>
   <td align="center">2021</td>
   <td align="center"><sub>Wikipedia articles from 20 different domains</sub></td>
   <td align="center"><sub>320,272 samples</sub></td>
   <td align="center"><sub>1) aspect selection (section title), 2) summary generation (section paragraph)</sub></td>
   <td align="center">ROUGE, F1, UniEval</td>
 </tr>
 <tr>
   <td rowspan=3 align="center">Fact-checking</td>
  <td align="center"><a href="https://huggingface.co/datasets/BeIR/scifact">Scifact</a></td>
   <td align="center">2020</td>
   <td align="center"><sub>5,183 abstracts</sub></td>
   <td align="center"><sub>1409 claim-abstract pairs</sub></td>
   <td align="center"><sub>3-class classification (support/refutes/Noinfo)</sub></td>
  <td align="center">nDCG@10</td>
 </tr>
 <tr>
   <td align="center"><a href="https:// huggingface.co/datasets/fever">FEVER</a></td>
   <td align="center">2018</td>
   <td align="center"><sub>50,000 popular pages from wikipedia</sub></td>
   <td align="center"><sub>185,445 claims</sub></td>
   <td align="center"><sub>3-class classification</sub></td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https:// huggingface.co/datasets/fever/ feverous">Feverous</a></td>
   <td align="center">2021</td>
   <td align="center"><sub>wikipedia</sub></td>
   <td align="center"><sub>87,026 claims</sub></td>
   <td align="center"><sub>3-class classification/evidence retrieval</sub></td>
   <td align="center">Accuracy</td>
 </tr>


</table>
