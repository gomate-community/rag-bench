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

