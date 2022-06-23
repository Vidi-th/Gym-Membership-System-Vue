<template>
    <v-container>
        <canvas id="myChart" max-width="566px" max-height="284px"></canvas>
    </v-container>
</template>

<script>
import Chart from 'chart.js/auto'

export default{
    mounted(){
        const ctx = document.getElementById('myChart');
        const myChart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: [
                    'Mei',
                    'Jun',
                    'Jul',
                    'Aug',
                    'Sept',
                ],
                datasets: [{
                    label: 'User',
                    data: [
                        62,
                        15,
                        0,
                        25,
                        10,
                    ],
                    backgroundColor: [
                        'rgba(86, 179, 245, 0.2)',
                        'rgba(161, 216, 255, 0.2)',
                    ],
                    borderColor: [
                        "#0291CB"
                    ],
                    borderWidth: 1,
                    fill:true,
                    tension: 0.3,
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                        
                    }
                }
            }
        });
        myChart;
    },
}
</script>
