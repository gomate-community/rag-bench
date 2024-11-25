# NarrativeQA benchmark

[NarrativeQA dataset](https://huggingface.co/datasets/narrativeqa) is an English-lanaguage dataset of stories and corresponding questions designed to test reading comprehension, especially on long documents. The dataset is used to test reading comprehension. There are 2 tasks proposed in the paper: "summaries only" and "stories only", depending on whether the human-generated summary or the full story text is used to answer the question.



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
	  <th align="center"> EM </th>
    </tr>
  </thead>
 <tbody>
 <!-- paper split -->

 <tr>
  <td rowspan=5><a href="https://arxiv.org/pdf/2406.13629"><sub>XXX </sub></a></td>
  <td rowspan=5>2024</td>
  <td rowspan=3><a href="https://github.com/weizhepei/InstructRAG">INSTRUCTRAG </a>

![](https://img.shields.io/github/stars/weizhepei/InstructRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:ChatGPT-4oMINI </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 71.6 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-70B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 70.8 </td>
 </tr>
  <tr>
  <td align="center">  R:DPR ,G:Llama-3-Ins-8B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 65.0 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins8B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 39.2 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins70B </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 54.2 </td>
 </tr>
 <!-- paper split -->
 

 </tbody>
</table>


### 2. LLM-based Methods (Reproducable)

