<script lang="ts">
    let email = "";
    let password = "";

    const getLoginInput = (event: Event) => {
        event.preventDefault(); // Prevent the form from submitting and reloading the page
        
        console.log("HALLLOOOO");
        console.log("Email:", email);
        console.log("Password:", password);
    };
</script>

<div class="flex relative items-center justify-center h-dvh w-full">
    <div class="flex flex-col items-center bg-white w-[25rem] h-[25rem] py-14 rounded-xl">
        <h2 class="text-2xl font-bold text-center text-black">Login</h2>

        <form class="w-full px-8 mt-4" on:submit={getLoginInput}>
            <div>
                <label class="block text-sm font-medium text-black" for="email">Email</label>
                <input
                    type="email"
                    bind:value={email}
                    id="email"
                    class="w-full px-4 py-2 mt-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
                    placeholder="Enter your email"
                    required
                />
            </div>

            <div class="py-5">
                <label class="block text-sm font-medium text-black" for="password">Password</label>
                <input
                    type="password"
                    bind:value={password}
                    id="password"
                    class="w-full px-4 py-2 mt-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
                    placeholder="Enter your password"
                    required
                />
            </div>

            <div class="py-6">
                <button
                    type="submit"
                    class="w-full px-4 py-2 text-white bg-blue-500 rounded-lg hover:bg-blue-600"
                >Login</button>
            </div>
        </form>
    </div>
</div>