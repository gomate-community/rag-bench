# NQ benchmark

[NQ dataset](https://huggingface.co/datasets/din0s/asqa) questions from real users, and it requires QA systems to read and comprehend an entire Wikipedia article that may or may not contain the answer to the question. The inclusion of real user questions, and the requirement that solutions should read an entire page to find the answer, cause NQ to be a more realistic and challenging task than prior QA datasets.  

## Performance

### 1. Leaderboard from SOTA

<table id="sortableTable">
 <thead>
    <tr>
	  <th align="center"> Model </th>
      <th align="center"> Year </th>
      <th align="center"> Paper </th>
      <th align="center">Retriever</th>
	  <th align="center">Generator</th>
	  <th align="center"> NDCG@10 </th>
	  <th align="center"> EM </th>
    </tr>
  </thead>
 <tbody>
 <tr>
  <td>BGM</td>
  <td>2024</td>
  <td><a href="https://arxiv.org/pdf/2401.06954"><sub>Bridging the Preference Gap between Retrievers and LLMs</sub></a></td>
  <td align="center"> "pre-given candiates" & T5-XXL (11B) </td>
  <td align="center"> PaLM2-S </td>
  <td align="center"> - </td>
  <td align="center"> 45.37 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline1}$$</td>
  <td>2024</td>
  <td><a href="https://arxiv.org/pdf/2401.06954"><sub>Bridging the Preference Gap between Retrievers and LLMs</sub></a></td>
  <td align="center"><a href="https://arxiv.org/pdf/2112.07899">GTR</a> </td>
  <td align="center"> PaLM2-S </td>
  <td align="center"> - </td>
  <td align="center"> 43.79 </td>
 </tr>
 <tr>
  <td>$$BGE_{Baseline2}$$</td>
  <td>2024</td>
  <td><a href="https://arxiv.org/pdf/2401.06954"><sub>Bridging the Preference Gap between Retrievers and LLMs</sub></a></td>
  <td align="center"> - </td>
  <td align="center"> PaLM2-S </td>
  <td align="center"> - </td>
  <td align="center"> 33.07 </td>
 </tr>

 </tbody>
</table>

<script>
  // Add sorting functionality
  document.addEventListener('DOMContentLoaded', () => {
    const table = document.getElementById('sortableTable');
    const headers = table.querySelectorAll('th');
    const rows = Array.from(table.querySelectorAll('tbody > tr'));

    headers.forEach((header, index) => {
      header.addEventListener('click', () => {
        const sortedRows = rows.sort((rowA, rowB) => {
          const cellA = rowA.children[index].textContent.trim();
          const cellB = rowB.children[index].textContent.trim();

          // Handle numeric and string comparison
          return !isNaN(cellA) && !isNaN(cellB)
            ? cellA - cellB
            : cellA.localeCompare(cellB);
        });

        // Append sorted rows to the tbody
        const tbody = table.querySelector('tbody');
        sortedRows.forEach(row => tbody.appendChild(row));
      });
    });
  });
</script>


### 2. LLM-based Methods (Reproducable)

