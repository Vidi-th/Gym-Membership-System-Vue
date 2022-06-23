<template>
    <v-container>
        <canvas id="bookingChart" max-width="566px" max-height="284px"></canvas>
    </v-container>
</template>

<script>
import Chart from 'chart.js/auto'

export default{
    mounted(){
        const ctx = document.getElementById('bookingChart');
        const bookingChart = new Chart(ctx, {
            type: 'line',
            data: {
                labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
                datasets: [{
                    label: 'Class',
                    data: [12, 19, 3, 5, 2, 3],
                    backgroundColor: [
                        'rgba(161, 216, 255, 0.2)',
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
        bookingChart;
    },
}
</script>
