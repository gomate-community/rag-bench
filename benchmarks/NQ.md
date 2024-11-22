# NQ benchmark

[NQ dataset](https://huggingface.co/datasets/din0s/asqa) questions from real users, and it requires QA systems to read and comprehend an entire Wikipedia article that may or may not contain the answer to the question. The inclusion of real user questions, and the requirement that solutions should read an entire page to find the answer, cause NQ to be a more realistic and challenging task than prior QA datasets.  

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
  <td rowspan=3><a href="https://arxiv.org/pdf/2401.06954"><sub>Bridging the Preference Gap between Retrievers and LLMs</sub></a></td>
  <td rowspan=3>2024</td>
  <td>BGM</td> <td align="center">  R: T5-XXL(11B), G: PaLM2-S </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 45.37 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R:<a href="https://arxiv.org/pdf/2112.07899">GTR</a>, G: PaLM2-S </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 43.79 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:,  G: PaLM2-S </td><td align="center"> - </td><td align="center"> - </td><td align="center"> 33.07 </td>
 </tr>
 <!-- paper split -->
 <tr>
  <td rowspan=5><a href="https://arxiv.org/pdf/2401.06954"><sub>ACTIVERAG: Autonomously Knowledge Assimilation and Accommodation through Retrieval-Augmented Agents </sub></a> <sub>(only sample 500 q for eval)</sub></td>
  <td rowspan=5>2024</td>
  <td><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:ChatGPT-4oMINI </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 71.6 </td>
 </tr>
  <tr>
  <td><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:Llama-3-Ins-70B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 70.8 </td>
 </tr>
  <tr>
  <td><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:DPR ,G:Llama-3-Ins-8B </td> <td align="center"> - </td> <td align="center"> - </td> <td align="center"> 65.0 </td>
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
 <tr>
  <td><a href="https://arxiv.org/pdf/2112.07899"><sub>Large Dual Encoders Are Generalizable Retrievers</sub></a></td>
  <td>2021</td>
  <td><a href="https://www.kaggle.com/models/google/gtr?tfhub-redirect=true">GTR</a></td>
  <td align="center"> R: GTR-XXL(4.8B),G: :x: </td>
  <td align="center"> 56.8 </td>
  <td align="center"> - </td>
  <td align="center"> - </td>
 </tr>

 </tbody>
</table>


### 2. LLM-based Methods (Reproducable)

