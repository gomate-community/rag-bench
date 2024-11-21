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
      <th align="center">Retriever</th>
	  <th align="center">Generator</th>
	  <th align="center"> NDCG@10 </th>
	  <th align="center"> EM </th>
    </tr>
  </thead>
 <tbody>
 <!-- paper split -->
 <tr>
  <td rowspan=3><a href="https://arxiv.org/pdf/2401.06954"><sub>Bridging the Preference Gap between Retrievers and LLMs</sub></a></td>
  <td rowspan=3>2024</td>
  <td>BGM</td> <td align="center">  T5-XXL(11B) </td> <td align="center"> PaLM2-S </td> <td align="center"> - </td> <td align="center"> 45.37 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline1}$$</td>
  <td align="center"><a href="https://arxiv.org/pdf/2112.07899">GTR</a> </td><td align="center"> PaLM2-S </td><td align="center"> - </td><td align="center"> 43.79 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline2}$$</td>
  <td align="center"> - </td><td align="center"> PaLM2-S </td><td align="center"> - </td><td align="center"> 33.07 </td>
 </tr>
 <!-- paper split -->
 <tr>
  <td rowspan=3><a href="https://arxiv.org/pdf/2401.06954"><sub>ACTIVERAG: Autonomously Knowledge Assimilation and Accommodation through Retrieval-Augmented Agents</sub></a></td>
  <td rowspan=3>2024</td>
  <td><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a> \n\n [code](https://github.com/lovodkin93/attribute-first-then-generate): ![](https://img.shields.io/github/stars/lovodkin93/attribute-first-then-generate.svg?style=social) \n\n </td> <td align="center">  T5-XXL(11B) </td> <td align="center"> PaLM2-S </td> <td align="center"> - </td> <td align="center"> 45.37 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline1}$$</td>
  <td align="center"><a href="https://arxiv.org/pdf/2112.07899">GTR</a> </td><td align="center"> PaLM2-S </td><td align="center"> - </td><td align="center"> 43.79 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline2}$$</td>
  <td align="center"> - </td><td align="center"> PaLM2-S </td><td align="center"> - </td><td align="center"> 33.07 </td>
 </tr>
 <!-- paper split -->
 <tr>
  <td><a href="https://arxiv.org/pdf/2112.07899"><sub>Large Dual Encoders Are Generalizable Retrievers</sub></a></td>
  <td>2021</td>
  <td><a href="https://www.kaggle.com/models/google/gtr?tfhub-redirect=true">GTR</a></td>
  <td align="center"> GTR-XXL(4.8B) </td>
  <td align="center"> - </td>
  <td align="center"> 56.8 </td>
  <td align="center"> - </td>
 </tr>

 </tbody>
</table>


### 2. LLM-based Methods (Reproducable)

