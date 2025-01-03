# PopQA benchmark

[PopQA dataset](https://huggingface.co/datasets/akariasai/PopQA) is a large-scale open-domain question answering (QA) dataset, consisting of 14k entity-centric QA pairs. Each question is created by converting a knowledge tuple retrieved from Wikidata using a template. Each question come with the original subject\_entitiey, object\_entityand relationship_type annotation, as well as Wikipedia monthly page views.

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
	  <th align="center"> Recall@5 </th>
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

</td> <td align="center">  R:Contriever ,G:Llama3-Ins-8B(FT) </td> <td align="center"> - </td> <td align="center"> 68.7 </td> <td align="center"> 66.2 </td>
 </tr>
  <tr>
  <td align="center">  R:Contriever ,G:Llama3-Ins-8B(ICL) </td> <td align="center"> - </td> <td align="center"> 68.7 </td> <td align="center"> 64.2</td>
 </tr>
 <tr>
  <td>NaiveRAG</td>
  <td align="center"> R: Contriever, G: ChatGPT </td><td align="center"> - </td><td align="center"> 68.7 </td><td align="center"> 50.8 </td>
 </tr>
 <tr>
  <td> NaiveRAG </td>
  <td align="center"> R: Contriever, G: Llama3-Ins8B </td><td align="center"> - </td><td align="center"> 68.7 </td><td align="center"> 62.3 </td>
 </tr>
 <!-- paper split -->
 <tr>
  <td rowspan=5><a href="https://arxiv.org/pdf/2401.06954"><sub>ACTIVERAG: Autonomously Knowledge Assimilation and Accommodation through Retrieval-Augmented Agents </sub></a> <sub>(only sample 500 q for eval)</sub></td>
  <td rowspan=5>2024</td>
  <td rowspan=3><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:ChatGPT-4oMINI </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 70.8 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-70B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 69.8 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-8B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 65.8 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins8B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 24.2 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins70B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 34.2 </td>
 </tr>
 <!-- paper split -->
  <!-- paper split -->
 <tr>
  <td rowspan=4><a href="https://arxiv.org/pdf/2310.11511"><sub>SELF-RAG: Learning To Retrieve, Generate, and Critique  Through SELF-Reflection </sub></a></td>
  <td rowspan=4>2023</td>
  <td rowspan=2><a href="https://github.com/AkariAsai/self-rag">Self-RAG </a>

![](https://img.shields.io/github/stars/AkariAsai/self-rag.svg?style=social)

</td> <td align="center">  R: Contriever ,G: Llama2-13B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 55.8 </td>
 </tr>
  <tr>
  <td align="center">  R: Contriever ,G:Llama2-7B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 54.9 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama2-7B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 14.7 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama2-13B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 14.7</td>
 </tr>
 <!-- paper split -->
 </tbody>
</table>


### 2. LLM-based Methods (Reproducable)

