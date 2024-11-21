# ASQA benchmark

[ASQA dataset](https://huggingface.co/datasets/din0s/asqa) is a question-answering dataset that contains factoid questions and long-form answers. The benchmark evaluates the correctness of the answer in the dataset. All detailed results can be download from [this repo](https://huggingface.co/datasets/golaxy/rag-bench/viewer/asqa). 

## Performance

### 1. Leaderboard from SOTA (reproducable)

<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center"> Model </th>
      <th align="center"> Year </th>
      <th align="center"> Paper </th>
      <th align="center">String EM</th>
	  <th align="center">Rouge L</th>
	  <th align="center"> Disambig F1 </th>
	  <th align="center">D-R Score</th>
    </tr>
  </thead>
 <tbody>
 <tr>
  <td><a href="XXX">XXX</a></td>
  <td>2024</td>
  <td> - </td>
  <td align="center"> - </td>
  <td align="center"> - </td>
  <td align="center"> - </td>
  <td align="center"> - </td>
 </tr>

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
