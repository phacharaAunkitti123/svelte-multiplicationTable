<script>
    let number = 1;
</script>

<div>
    <h2 class="header">Phachara Multiplication Table</h2>
</div>

<div class="input-container">
    <label>
        Enter a number:
        <input type="number" bind:value={number} />
    </label>
</div>

{#if number}
    <table>
        <tr>
            <th>Multiplier</th>
            <th>Result</th>
        </tr>
        {#each Array.from({ length: 12 }, (_, i) => i + 1) as factor}
            <tr>
                <td>{number} x {factor}</td>
                <td>{number * factor}</td>
            </tr>
        {/each}
    </table>
{/if}

<style>
    .header {
        text-align: center;
        font-size: 20px;
    }

    .input-container {
        text-align: center;
    }

    label {
        font-size: 18px;
    }

    input {
        padding: 8px;
        border: 1px solid #ccc;
        border-radius: 4px;
    }

    table {
        border-collapse: collapse;
        border-radius: 5px;
        width: 80%;
        margin: 20px auto;
    }

    th,
    td {
        border: 1px solid #ccc;
        padding: 8px;
        text-align: center;
    }

    th {
        background-color: #495e57;
        color: white;
    }

    tr:nth-child(odd) {
        background-color: #f5f7f8;
    }

    tr:hover {
        background-color: #f4ce14;
    }
</style>
