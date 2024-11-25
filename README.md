# rag-bench

Rag-Bench is a toolkit derived from [Rageval](https://github.com/gomate-community/rageval) to evaluate Retrieval Augmented Generation (RAG) system, consisting of 4 benchmarks and datasets. All benchmark results could be easily reproduced with the tool.

## Benchmarks


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
  <td align="center"><a href="./benchmarks/NQ.md">Natural Questions (NQ)</a></td>
  <td align="center">Generator, Retriever</td>
  <td align="center">Rouge, EM</td>
 </tr>
 <tr>
  <td align="center"><a href="./benchmarks/TriviaQA.md">TriviaQA</a></td>
  <td align="center">Generator</td>
  <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/NarrativeQA.md">NarrativeQA (NQA)</a></td>
   <td align="center">Generator</td>
   <td align="center">Rouge</td>
 </tr>
 <tr>
   <td align="center"><a href="https://huggingface.co/datasets/rajpurkar/squad">SQuAD</a></td>
   <td align="center">Generator</td>
   <td align="center">EM</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/PopQA.md">PopQA</a></td>
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
  <td align="center"><a href="./benchmarks/2WikiMHQA.md">2WikiMultihopQA</a></td>
  <td align="center">Generator</td>
  <td align="center">F1</td>
 </tr>
 <tr>
   <td align="center"><a href="./benchmarks/HotpotQA">HotpotQA</a></td>
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
   <td align="center"><a href="./benchmarks/ASQA.md">ASQA</a></td>
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
