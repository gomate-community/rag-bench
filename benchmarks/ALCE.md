# ALCE benchmark

[ALCE](https://github.com/princeton-nlp/ALCE) is a benchmark for Automatic LLMs' Citation Evaluation. ALCE contains three datasets: ASQA, QAMPARI, and ELI5. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/alce_eli5_bm25). Besides, these results can be reproduced based on [the script](./benchmarks/ALCE/ASQA/run.sh) in this repo.

## Performance

### 1. Leaderboard from SOTA

#### 1.1 ASQA dataset
<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center" style="width:246px;"> Paper </th>
      <th align="center"> Year </th>
      <th align="center"> Model </th>
      <th align="center">Model Details</th>
	  <th align="center"> precision </th>
	  <th align="center"> recall </th>
	  <th align="center"> str-EM </th>
	  <th align="center"> rouge </th>
      <th align="center"> MAUVE </th>
    </tr>
  </thead>
 <tbody>
 <!-- paper split -->
 <tr>
  <td rowspan=4><a href="https://arxiv.org/pdf/2310.11511"><sub>SELF-RAG: Learning To Retrieve, Generate, and Critique  Through SELF-Reflection </sub></a></td>
  <td rowspan=4>2024</td>
  <td rowspan=2><a href="https://github.com/AkariAsai/self-rag">Self-RAG </a>

![](https://img.shields.io/github/stars/AkariAsai/self-rag.svg?style=social)

</td> <td align="center">  R: GTR-XXL ,G: Llama2-13B </td> <td align="center"> 70.3 </td> <td align="center"> 71.3 </td> <td align="center"> 31.7 </td><td align="center"> 37.0 </td><td align="center"> 71.6 </td>
 </tr>
  <tr>
  <td align="center">  R: GTR-XXL ,G:Llama2-7B </td> <td align="center"> 66.9 </td> <td align="center"> 67.8 </td> <td align="center"> 30.0 </td><td align="center"> 35.7 </td><td align="center"> 74.3 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama2-7B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 7.9 </td><td align="center"> 15.3 </td><td align="center"> 19.0 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama2-13B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 7.2</td><td align="center"> 12.4</td><td align="center"> 16.0</td>
 </tr>
 <!-- paper split -->
 

 </tbody>
</table>

### 2. LLM-based Methods (reproducable)

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
