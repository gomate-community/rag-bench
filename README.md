# rag-bench

Rag-Bench is a toolkit derived from [Rageval](https://github.com/gomate-community/rageval) to evaluate Retrieval Augmented Generation (RAG) system, consisting of 4 benchmarks and datasets. All benchmark results could be easily reproduced with the tool.

## Benchmarks

### 1. [ASQA benchmark](benchmarks/ASQA/README.md)

[ASQA dataset](https://huggingface.co/datasets/din0s/asqa) is a question-answering dataset that contains factoid questions and long-form answers. The benchmark evaluates the correctness of the answer in the dataset. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa). Besides, these results can be reproduced based on [the script](./benchmarks/ASQA/run.sh) in this repo.


<table>
 <col width=166>
 <col width=125>
 <col width=125 span=4>
 <tr>
  <td rowspan=2 align="center"><b>Model</b></td>
  <td rowspan=2 align="center"><b>Retriever</b></td>
  <td colspan=4 align="center"><b>Metric</b></td>
 </tr>
 <tr>
  <td align="center"><a href="rageval\metrics\_answer_exact_match.py">String EM</a></td>
  <td align="center"><a href="rageval\metrics\_answer_rouge_correctness.py">Rouge L</a></td>
  <td align="center"><a href="rageval\metrics\_answer_disambig_f1.py">Disambig F1</a></td>
  <td align="center"><a href="benchmarks\ASQA\asqa_benchmark.py">D-R Score</a></td>
 </tr>
 <tr>
  <td>gpt-3.5-turbo-instruct</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/gpt_3.5_turbo_instruct">no-retrieval</a></td>
  <td align="center">33.8</td>
  <td align="center">30.2</td>
  <td align="center">30.7</td>
  <td align="center">30.5</td>
 </tr>
 <tr>
  <td>mistral-7b</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/mistral_7b">no-retrieval</a></td>
  <td align="center">20.6</td>
  <td align="center">31.1</td>
  <td align="center">26.6</td>
  <td align="center">28.7</td>
 </tr>
 <tr>
  <td>llama2-7b-chat</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/llama2_7b_chat">no-retrieval</a></td>
  <td align="center">21.7</td>
  <td align="center">30.7</td>
  <td align="center">28.0</td>
  <td align="center">29.3</td>
 </tr>
 <tr>
  <td>solar-10.7b-instruct</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/solar_10.7b_instruct">no-retrieval</a></td>
  <td align="center">23.0</td>
  <td align="center">24.9</td>
  <td align="center">28.1</td>
  <td align="center">26.5</td>
 </tr>
</table>

### 2. [ALCE Benchmark](benchmarks/ALCE)

[ALCE](https://github.com/princeton-nlp/ALCE) is a benchmark for Automatic LLMs' Citation Evaluation. ALCE contains three datasets: ASQA, QAMPARI, and ELI5. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/alce_eli5_bm25). Besides, these results can be reproduced based on [the script](./benchmarks/ALCE/ASQA/run.sh) in this repo.

<table>
 <col width=75>
 <col width=125>
 <col width=85>
 <col width=145>
 <col width=125 span=5>
 <tr>
  <td rowspan=2 align="center"><b>Dataset</b></td>
  <td rowspan=2 align="center"><b>Model</b></td>
  <td colspan=2 align="center"><b>Method</b></td>
  <td colspan=5 align="center"><b>Metric</b></td>
 </tr>
 <tr>
  <td align="center">retriever</td>
  <td align="center">prompt</td>
  <td align="center">MAUVE</td>
  <td align="center"><a href="rageval\metrics\_answer_exact_match.py">EM Recall</a></td>
  <td align="center"><a href="rageval\metrics\_answer_claim_recall.py">Claim Recall</a></td>
  <td align="center"><a href="rageval\metrics\_answer_citation_recall.py">Citation Recall</a></td>
  <td align="center"><a href="rageval\metrics\_answer_citation_precision.py">Citation Precision</a></td>
 </tr>
 <tr>
  <!-- <td rowspan=7><a href="benchmarks/ALCE/ASQA/README.md">ASQA</a></td>
  <td rowspan=7>llama2-7b-chat</td>
  <td rowspan=5>GTR</td>   -->
  <td rowspan=3 style="text-align:left;padding-left:10px"><a href="benchmarks/ALCE/ASQA/README.md">ASQA</a></td>
  <td rowspan=3>llama2-7b-chat</td>
  <td rowspan=1>GTR</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/alce_asqa_gtr">vanilla(5-psg)</a></td>
  <td align="center">-</td>
  <td align="center">33.3</td>
  <td align="center">-</td>
  <td align="center">55.9</td>
  <td align="center">80.0</td>
 </tr>
 <!-- <tr>
  <td>summary(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>summary(10-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>snippet(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>snippet(10-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr> -->
 <tr>
  <td>DPR</td>
  <td>vanilla(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
 <tr>
  <td>Oracle</td>
  <td>vanilla(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
 <tr>
  <!-- <td rowspan=6><a href="benchmarks/ALCE/ELI5/README.md">ELI5</a></td>
  <td rowspan=6>llama2-7b-chat</td>
  <td rowspan=5>BM25</td> -->
  <td rowspan=3><a href="benchmarks/ALCE/ELI5/README.md">ELI5</a></td>
  <td rowspan=3>llama2-7b-chat</td>
  <td rowspan=1>BM25</td>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/alce_eli5_bm25">vanilla(5-psg)</a></td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">11.5</td>
  <td align="center">26.6</td>
  <td align="center">74.5</td>
 </tr>
 <!-- <tr>
  <td>summary(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>summary(10-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>snippet(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
  <tr>
  <td>snippet(10-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr> -->
 <tr>
  <td>Oracle</td>
  <td>vanilla(5-psg)</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
  <td align="center">-</td>
 </tr>
</table>

## Datasets

Here are datasets with the corresponding metrics.

<table>
 <tr>
  <td rowspan=1 align="center"><b>Task</b></td>
  <td colspan=1 align="center"><b>Dataset Name</b></td>
  <td rowspan=1 align="center"><b>RAG Module</b></td>
  <td colspan=1 align="center"><b>Metrics</b></td>
 </tr>
 <tr>
  <td rowspan=8 align="center">QA</td>
  <td align="center"><a href="https://huggingface.co/datasets/natural_questions">Natural Questions (NQ)</a></td>
  <td align="center">Generator, Retriever</td>
  <td align="center">Rouge, EM</td>
 </tr>
 <tr>
  <td align="center"><a href="https://huggingface.co/datasets/mandarjoshi/trivia_qa">TriviaQA</a></td>
  <td align="center">Generator</td>
  <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/narrativeqa">NarrativeQA (NQA)</a></td>
   <td align="center">Generator</td>
   <td align="center">Rouge</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/rajpurkar/squad">SQuAD</a></td>
   <td align="center">Generator</td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/akariasai/PopQA">PopQA</a></td>
   <td align="center">Generator, Rewriter</td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/Rowan/ hellaswag">HellaSwag</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https://allenai. org/data/strategyqa">StrategyQA</a></td>
   <td align="center">Generator</td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://allenai. org/data/fermi">Fermi</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>

 <tr>
  <td rowspan=2 align="center">Multi-Hop QA</td>
  <td align="center"><a href="https://github.com/Alab-NII/2wikimultihop">2WikiMultihopQA</a></td>
  <td align="center">Generator</td>
  <td align="center">F1</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/hotpot_qa">HotpotQA</a></td>
   <td align="center">Generator, Rewriter</td>
   <td align="center">F1</td>
 </tr>
 <tr>
  <td rowspan=4 align="center">Long-Form QA</td>
  <td align="center"><a href="https://huggingface.co/datasets/eli5">ELI5</a></td>
  <td align="center">Generator</td>
  <td align="center">Citation Recall, Citation Precision, Claim Recall</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/explodinggradients/WikiEval">WikiEval</a></td>
   <td align="center">Generator</td>
   <td align="center">Ragas</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/din0s/asqa">ASQA</a></td>
   <td align="center">Generator</td>
   <td align="center">disambig F1, RougeL, EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/THUDM/webglm-qa">WebGLM</a></td>
   <td align="center">Generator</td>
   <td align="center">RougeL, Citation Recall, Citation Precision</td>
 </tr>
 <tr>
   <td rowspan=4 align="center">Multiple Choice</td>
   <td align="center"><a href="https://huggingface.co/datasets/truthful_qa">TruthfulQA</a></td>
   <td align="center">Generator</td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/cais/mmlu">MMLU</a></td>
   <td align="center">Generator, Rewriter</td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/allenai/openbookqa">OpenBook QA</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https://github.com/nyu-mll/quality">QuALITY (QLTY)</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td rowspan=1 align="center">Open-Domain Summarization</td>
   <td align="center"><a href="https://huggingface.co/datasets/wiki_asp">WikiAsp</a></td>
   <td align="center">Generator</td>
   <td align="center">ROUGE, F1, UniEval</td>
 </tr>
 <tr>
   <td rowspan=3 align="center">Fact-checking</td>
  <td align="center"><a href="https://huggingface.co/datasets/BeIR/scifact">Scifact</a></td>
  <td align="center">Rewriter</td>
  <td align="center">nDCG@10</td>
 </tr>
 <tr>
   <td align="center"><a href="https:// huggingface.co/datasets/fever">FEVER</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>
 <tr>
   <td align="center"><a href="https:// huggingface.co/datasets/fever/ feverous">Feverous</a></td>
   <td align="center">Generator</td>
   <td align="center">Accuracy</td>
 </tr>


</table>
