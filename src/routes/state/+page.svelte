<script>
    let name = $state("Fathin")
    let umur = $state()

    let data = $state.raw({
        name: "Fadhil",
        umur: 1
    })

    data = {
        name: "Fad",
        umur: 78
    }

    class Hitung {
        count = $state(0)

        tambah = () => { this.count++ }

        kurang = () => { this.count-- }

        reset = () => { this.count = 0 }

    }
    
    let hitung = new Hitung()

</script>

<main class="p-3 grid grid-cols-3">

    <!-- Contoh  Informasi Pribadi -->
    <div class="flex flex-col gap-5">

        <!-- Reactive -->
        <div class="flex gap-5">
            <div>
                <h1>Name</h1>
                <h1>Umur</h1>
            </div>
            <div>
                <h1>:</h1>
                <h1>:</h1>
            </div>
            <div>
                <h1>{ name }</h1>
                <div class="flex gap-5">
                    <h1>{ umur ? umur : "-" }</h1>
                    <input bind:value={umur} class="border rounded-md px-3" type="number" placeholder="Masukkan Usia">
                </div>
            </div> 
        </div>

        <!-- Cannot Change -->
        <div class="flex gap-5">
            <div>
                <h1>Name</h1>
                <h1>Umur</h1>
            </div>
            <div>
                <h1>:</h1>
                <h1>:</h1>
            </div>
            <div>
                <h1>{ data.name }</h1>
                <div class="flex gap-5">
                    <h1>{ data.umur ? data.umur : "-" }</h1>
                    <input bind:value={data.umur} class="border rounded-md px-3" type="number" placeholder="Masukkan Usia">
                </div>
            </div> 
        </div>

    </div>

    <!-- Count -->
    <div class="flex justify-center flex-col items-center">
        <h1 class="text-4xl">{ hitung.count }</h1>
        <div class="flex gap-5">
            <button onclick={() => hitung.kurang()} class="text-white bg-gray-800 rounded-lg w-40">-</button>
            <button onclick={() => hitung.reset()} class="font-bold text-2xl">Reset</button>
            <button onclick={() => hitung.tambah()} class="text-white bg-gray-800 rounded-lg w-40">+</button>
        </div>
    </div>
</main>