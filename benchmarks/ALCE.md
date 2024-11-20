# ALCE benchmark

[ALCE](https://github.com/princeton-nlp/ALCE) is a benchmark for Automatic LLMs' Citation Evaluation. ALCE contains three datasets: ASQA, QAMPARI, and ELI5. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/alce_eli5_bm25). Besides, these results can be reproduced based on [the script](./benchmarks/ALCE/ASQA/run.sh) in this repo.

## Performance

### 1. LLM-based Methods

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
