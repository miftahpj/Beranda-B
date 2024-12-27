<script setup lang="ts">
import Chart from 'chart.js/auto';

const labels = [
    'Angkatan 10',
    'Angkatan 11',
    'Angkatan 12',
  ];

  const data = {
    labels: labels,
    datasets: [{
      label: 'Jumlah',
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [540, 540, 540],
    }]
  };


  const config = {
    type: 'bar',
    data: data,
    options: {}
  };

onMounted(() => {
    const myChart = new Chart(
    document.getElementById('Chart'),
    config
  );
})
</script>

<template>
    <div class="pt-5">
        <canvas id="Chart"></canvas>
      </div>
      
</template>