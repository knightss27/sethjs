<script>
    export let isOpen = false;


</script>

<main>
    <div class="dropdown">
        <button class="dropbtn" on:click={() => {isOpen = !isOpen}} class:dropbtn-active={isOpen} >Dropdown</button>
        {#if isOpen}
            <div class="dropdown-content">
    <!--            TODO: Global classes for these -->
                <a href="#">Link 1</a>
                <a href="#">Link 2</a>
                <a href="#">Link 3</a>
            </div>
        {/if}
    </div>
</main>

<style>
    .dropbtn {
        color: white;
        font-size: 16px;
        cursor: pointer;
        border: 1px solid white;
        border-radius: 15px;
        margin: 2px;
        padding: 10px;
        background: transparent;
        transition: ease border-radius 0.1s;
    }

    .dropdown {
        position: relative;
        display: inline-block;
    }

    .dropdown-content {
        position: absolute;
        background-color: #f9f9f9;
        min-width: 160px;
        box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
        z-index: 1;
        display: block;
    }

    .dropdown-content a {
        color: black;
        padding: 12px 16px;
        text-decoration: none;
        display: block;
    }

    .dropdown-content a:hover {
        background-color: #f1f1f1;
    }

    .dropbtn-active {
        background-color: #474747;
        border-radius: 15px 15px 0 0;
    }

    .dropbtn:active {
        transform: scale(95%, 95%);
    }
</style>