<script>
    export let name = "";
</script>

<main>
    <label>
        <select name={name}>
            <slot></slot>
        </select>
    </label>
</main>

<style>
    select {
        border: 1px solid white;
        border-radius: 15px;
        margin: 2px;
        padding: 10px;
        background: transparent;
        color: white;
        outline: none;
        display: inline-block;
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
        cursor: pointer;
        width: 50%;
    }

    @media screen and (-webkit-min-device-pixel-ratio: 0) {
        select {
            padding-right: 18px
        }
    }

    label {
        position: relative;
    }

    label:after {
        content: '<>';
        font-size: 13px;
        color: #aaa;
        -webkit-transform: rotate(90deg);
        -moz-transform: rotate(90deg);
        -ms-transform: rotate(90deg);
        transform: rotate(90deg);
        right: 8px;
        top: 2px;
        padding: 0 0 2px;
        border-bottom: 1px solid #ddd;
        position: absolute;
        pointer-events: none;
    }

    label:before {
        content: '';
        right: 6px;
        top: 0;
        width: 20px;
        height: 20px;
        position: absolute;
        pointer-events: none;
        display: block;
    }
</style>