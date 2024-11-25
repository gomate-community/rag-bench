# 2WikiMultiHopQA benchmark

[2WikiMultiHopQA dataset](https://github.com/Alab-NII/2wikimultihop) is a multi-hop QA dataset, which uses structured and unstructured data. This dataset introduces the evidence information containing a reasoning path for multi-hop questions. The evidence information has two benefits: (i) providing a comprehensive explanation for predictions and (ii) evaluating the reasoning skills of a model. 


## Performance

### 1. Leaderboard from SOTA

<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center" style="width:246px;"> Paper </th>
      <th align="center"> Year </th>
      <th align="center"> Model </th>
      <th align="center">Model Details</th>
	  <th align="center"> NDCG@10 </th>
	  <th align="center"> Recall@10 </th>
	  <th align="center"> acc </th>
    </tr>
  </thead>
 <tbody>
 <!-- paper split -->

 <tr>
  <td rowspan=4><a href="https://arxiv.org/pdf/2406.13629"><sub>INSTRUCTRAG: Instructing Retrieval-Augmented Generation via Self-Synthesized Rationales </sub></a></td>
  <td rowspan=4>2024</td>
  <td rowspan=2><a href="https://github.com/weizhepei/InstructRAG">InstructRAG </a>

![](https://img.shields.io/github/stars/weizhepei/InstructRAG.svg?style=social)

</td> <td align="center">  R:BM25 ,G:Llama3-Ins-8B(FT) </td> <td align="center"> - </td> <td align="center"> 40.7 </td> <td align="center"> 57.2 </td>
 </tr>
  <tr>
  <td align="center">  R: BM25 ,G:Llama3-Ins-8B(ICL) </td> <td align="center"> - </td> <td align="center"> 40.7 </td> <td align="center"> 50.4</td>
 </tr>
 <tr>
  <td>NaiveRAG</td>
  <td align="center"> R: BM25, G: Llama3-Ins70B </td><td align="center"> - </td><td align="center"> 40.7 </td><td align="center"> 51.2 </td>
 </tr>
 <tr>
  <td> NaiveRAG </td>
  <td align="center"> R: BM25, G: Llama3-Ins8B </td><td align="center"> - </td><td align="center"> 40.7 </td><td align="center"> 43.4 </td>
 </tr>
 <!-- paper split -->
 <tr>
  <td rowspan=5><a href="https://arxiv.org/pdf/2401.06954"><sub>ACTIVERAG: Autonomously Knowledge Assimilation and Accommodation through Retrieval-Augmented Agents </sub></a> <sub>(only sample 500 q for eval)</sub></td>
  <td rowspan=5>2024</td>
  <td rowspan=3><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:ChatGPT-4oMINI </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 59.6 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-70B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 61.2 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-8B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 52.2 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins8B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 43.0 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins70B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 53.8 </td>
 </tr>
 <!-- paper split -->

 </tbody>
</table>


### 2. LLM-based Methods (Reproducable)

