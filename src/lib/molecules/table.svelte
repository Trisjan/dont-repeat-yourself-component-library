<script>
    export let tableData
</script>
<section>
    <table>
        <thead>
            {#each Object.keys(tableData[0]) as columnheading}
                <th>{columnheading}</th>
            {/each}
        </thead>
        <tbody>
            {#each Object.values(tableData) as row}
                <tr>
                    {#each Object.values(row) as cell}
                        <td>{cell}</td>
                    {/each}
                </tr>
            {/each}
        </tbody>
    </table>
</section>
<style>
    section {
        overflow-x: auto;
    }

    table {
        border-spacing: 0;
        border-collapse: collapse;
        width: 100%;
        border-radius: 10px;
        background-color: white;
    }

    thead {
        background-color: #E4E9F7;
    }

    tbody {
        padding-bottom: 2rem;
    }
    
    th, td {
        text-align: left;
        padding: 8px 8px 8px 2.5rem;
    }

    table tr {
        border-bottom: 1px solid rgb(192, 198, 200, 0.5);
    }

    table tr:last-child {
        border-bottom: none;
    }
    </style>