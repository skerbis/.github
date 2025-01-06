<details>
<summary>Redaxo Tag Countdown</summary>

<div id="redaxo-countdown">Countdown lädt...</div>

<script>
function updateCountdown() {
    const targetDate = new Date('2025-01-25T00:00:00');
    const now = new Date();
    const difference = targetDate.getTime() - now.getTime();

    if (difference > 0) {
        const days = Math.floor(difference / (1000 * 60 * 60 * 24));
        const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((difference % (1000 * 60)) / 1000);

        document.getElementById('redaxo-countdown').textContent = 
            `Redaxo Tag in: ${days} Tagen, ${hours} Std, ${minutes} Min, ${seconds} Sek`;
    }
}

updateCountdown();
setInterval(updateCountdown, 1000);
</script>
</details>
