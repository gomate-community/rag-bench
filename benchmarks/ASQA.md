# ASQA benchmark

[ASQA dataset](https://huggingface.co/datasets/din0s/asqa) is a question-answering dataset that contains factoid questions and long-form answers. The benchmark evaluates the correctness of the answer in the dataset. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa). 

## Performance

### 1. Leaderboard from SOTA

<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center" style="width:246px;"> Paper </th>
      <th align="center"> Year </th>
      <th align="center"> Model </th>
      <th align="center">Model Details</th>
	  <th align="center"> hit rates </th>
	  <th align="center"> recall </th>
	  <th align="center"> str-EM </th>
    </tr>
  </thead>
 <tbody>
  <!-- paper split -->
 <tr>
  <td rowspan=4><a href="https://arxiv.org/pdf/2406.13629"><sub>INSTRUCTRAG: Instructing Retrieval-Augmented Generation via Self-Synthesized Rationales </sub></a></td>
  <td rowspan=4>2024</td>
  <td rowspan=2><a href="https://github.com/weizhepei/InstructRAG">InstructRAG </a>

![](https://img.shields.io/github/stars/weizhepei/InstructRAG.svg?style=social)

</td> <td align="center">  R:GTR ,G:Llama3-Ins-8B(FT) </td> <td align="center"> - </td> <td align="center"> 65.7 </td> <td align="center"> 70.5 </td>
 </tr>
  <tr>
  <td align="center">  R: GTR ,G:Llama3-Ins-8B(ICL) </td> <td align="center"> - </td> <td align="center"> 70.9 </td> <td align="center"> 74.1</td>
 </tr>
 <tr>
  <td>NaiveRAG</td>
  <td align="center"> R: GTR, G: ChatGPT </td><td align="center"> - </td><td align="center"> 65.1 </td><td align="center"> 76.6 </td>
 </tr>
 <tr>
  <td> NaiveRAG </td>
  <td align="center"> R: GTR, G: Llama3-Ins8B </td><td align="center"> - </td><td align="center"> 62.1 </td><td align="center"> 66.4 </td>
 </tr>
 <!-- paper split -->
 <!-- paper split -->
 <tr>
  <td rowspan=5><a href="https://arxiv.org/pdf/2401.06954"><sub>ACTIVERAG: Autonomously Knowledge Assimilation and Accommodation through Retrieval-Augmented Agents </sub></a> <sub>(only sample 500 q for eval)</sub></td>
  <td rowspan=5>2024</td>
  <td rowspan=3><a href="https://github.com/OpenMatch/ActiveRAG">ActiveRAG </a>

![](https://img.shields.io/github/stars/OpenMatch/ActiveRAG.svg?style=social)

</td> <td align="center">  R:GTR ,G:ChatGPT-4oMINI </td> <td align="center"> 25.6 </td> <td align="center"> 62.0 </td> <td align="center"> 52.7 </td>
 </tr>
  <tr>
  <td align="center">  R:GTR ,G:Llama-3-Ins-70B </td> <td align="center"> 23.8 </td> <td align="center"> 59.7 </td> <td align="center"> 50.4 </td>
 </tr>
  <tr>
  <td align="center">  R:GTR ,G:Llama-3-Ins-8B </td> <td align="center"> 20.4 </td> <td align="center"> 57.7 </td> <td align="center"> 45.7 </td>
 </tr>
 <tr>
  <td>Baseline1</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins8B </td><td align="center"> 5.0 </td><td align="center"> 16.1 </td><td align="center"> 24.8 </td>
 </tr>
 <tr>
  <td>Baseline2</td>
  <td align="center"> R: :x:, G: Llama3-8-Ins70B </td><td align="center"> 8.8 </td><td align="center"> 20.0 </td><td align="center"> 33.3 </td>
 </tr>
 <!-- paper split -->
 

 </tbody>
</table>


### 2. LLM-based Methods (reproducable)

These results can be reproduced based on [the script](./benchmarks/ASQA/run.sh) in this repo.

<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center"> Model </th>
      <th align="center"> Year </th>
      <th align="center"> Retriever </th>
      <th align="center">String EM</th>
	  <th align="center">Rouge L</th>
	  <th align="center"> Disambig F1 </th>
	  <th align="center">D-R Score</th>
    </tr>
  </thead>
 <tbody>
 <tr>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/gpt_3.5_turbo_instruct">gpt-3.5-turbo-instruct</a></td>
  <td>2024</td>
  <td>no-retrieval</td>
  <td align="center">33.8</td>
  <td align="center">30.2</td>
  <td align="center">30.7</td>
  <td align="center">30.5</td>
 </tr>
 <tr>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/mistral_7b">mistral-7b</a></td>
  <td>2023</td>
  <td>no-retrieval</td>
  <td align="center">20.6</td>
  <td align="center">31.1</td>
  <td align="center">26.6</td>
  <td align="center">28.7</td>
 </tr>
 <tr>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/llama2_7b_chat">llama2-7b-chat</a></td>
  <td>2023</td>
  <td>no-retrieval</td>
  <td align="center">21.7</td>
  <td align="center">30.7</td>
  <td align="center">28.0</td>
  <td align="center">29.3</td>
 </tr>
 <tr>
  <td><a href="https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa/solar_10.7b_instruct">solar-10.7b-instruct</a></td>
  <td>2024</td>
  <td>no-retrieval</td>
  <td align="center">23.0</td>
  <td align="center">24.9</td>
  <td align="center">28.1</td>
  <td align="center">26.5</td>
 </tr>
 </tbody>
</table>
