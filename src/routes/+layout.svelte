<script>
    import "@fontsource-variable/dm-sans";
    import "../app.css";

    let { data, children } = $props();
</script>

<nav class="navbar bg-base-100 shadow-sm spacing">
    <div class="navbar-start">
        <div class="dropdown">
            <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="h-5 w-5"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M4 6h16M4 12h8m-8 6h16"
                    />
                </svg>
            </div>
            <ul
                class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow"
            >
                <li><a href="/">Item 1</a></li>
                <li>
                    <a href="/">Parent</a>
                    <ul class="p-2">
                        <li><a href="/">Submenu 1</a></li>
                        <li><a href="/">Submenu 2</a></li>
                    </ul>
                </li>
                <li><a href="/">Item 3</a></li>
            </ul>
        </div>
        <a href="/" class="btn btn-ghost text-xl">daisyUI</a>
    </div>
    <div class="navbar-center hidden lg:flex">
        <ul class="menu menu-horizontal px-1">
            <li><a href="/">Item 1</a></li>
            <li>
                <details>
                    <summary>Parent</summary>
                    <ul class="p-2">
                        <li><a href="/">Submenu 1</a></li>
                        <li><a href="/">Submenu 2</a></li>
                    </ul>
                </details>
            </li>
            <li><a href="/">Item 3</a></li>
        </ul>
    </div>
    <div class="navbar-end">
        {#if !data.session}
            <a href="/" class="btn btn-accent">Sign in &rarr;</a>
        {:else}
            <div class="dropdown dropdown-end">
                <div
                    tabindex="0"
                    role="button"
                    class="btn btn-ghost btn-circle avatar"
                >
                    <div class="w-10 rounded-full">
                        <img
                            alt="Tailwind CSS Navbar component"
                            src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
                        />
                    </div>
                </div>
                <ul
                    tabindex="0"
                    class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow"
                >
                    <li>
                        <a class="justify-between">
                            Profile
                            <span class="badge">New</span>
                        </a>
                    </li>
                    <li><a>Settings</a></li>
                    <li><a>Logout</a></li>
                </ul>
            </div>
        {/if}
    </div>
</nav>
{@render children()}

<style>
    :global(body) {
        font-family: "DM Sans Variable", sans-serif;
    }
</style>
