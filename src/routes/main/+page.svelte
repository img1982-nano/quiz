<script lang="ts">
    let questions = [
        {
        "id": 1,
        "message": "パンはパンでもだべられないパンは？",
        "answer": "フライパン"
        },
        {
        "id": 2,
        "message": "黒ずくめの組織のリーダーは？",
        "answer": "ジン"
        },
        {
        "id": 3,
        "message": "MicrosoftのCEOは？",
        "answer": "マイケル・ジャクソン(嘘)"
        },
    ]
    function next(){
        if (answer === questions[question].answer) {
            alert("正解！おめでとう")
            location.reload()
        } else {
            alert(`不正解...正解は:${questions[question].answer}`)
            location.reload()
        }
    }
    let question: number = Math.floor(Math.random() * 3);
    let answer = ""
</script>
<h1 class="text-black text-mono text-3xl">問題:{questions[question].message}</h1>
<input bind:value={answer} class="border-blue-500"/>
<button class="bg-yellow-200 active:bg-yellow-400 rounded x-10 y-30" onclick={() => next()}>答え合わせ</button>
