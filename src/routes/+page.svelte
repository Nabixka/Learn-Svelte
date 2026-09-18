<script>
    let password = $state('')
    let isNum = $state(true)

    function generatePassword(){
        password = ''
        const abc = "abcdefghijklmnopqrstuvwxyz"

        while(password.length < 12){
            const randomIndex = Math.round(Math.random() * abc.length)
            password += abc.charAt(randomIndex)
        }
    }

</script>

<div id="buttonGenerate">
    <h1>Generate Password</h1>
    <button onclick={generatePassword} id="btn">Click</button>
</div>

<input type="checkbox" bind:checked={isNum}>

<h3>{password}</h3>

<style>
    #buttonGenerate{
        display: flex;
        gap: 5px;
    }

    #btn{
        background-color: gray;
        color: white;
    }
</style>