<template>
<div class="grid-container">
    <div class="header">
        header
    </div>
    <div class="menu">
        menu
    </div>
    <div class="aside">
        aside
    </div>
    <div class="booter">
        booter
    </div>

</div>
</template>

<script>
export default {
  name: 'HelloWorld'
}
</script>

<style>
* {
            margin: 0;
            padding: 0;
        }

        html {
            min-height: 100%;
        }

        body {
            min-height: 100%;
            position: relative;
        }

        body::before {
            z-index: -1;
            position: absolute;
            left: 0;
            top: 0;
            width: 100%;
            min-height: 100%;
            background-size: cover;
            background: url('../assets/background.jpg') repeat-y;
            content: '';
            display: block;
            filter: blur(30px);
        }

        .grid-container {
            margin: 20px;

            display: grid;
            grid-template-areas:
            'header  header header'
            'menu aside aside'
            'booter booter booter';
            grid-column-gap: 20px;
            grid-row-gap: 20px;
        }

        @media screen and (max-width: 700px) {
            .grid-container {
                 grid-template-areas:
                'header header header'
                'aside aside aside'
                'booter booter booter';
            }
            .menu{
                display: none !important;
            }

        }

        .header {
            grid-area: header;
            height: 80px;

        }

        .menu {
            grid-area: menu;
            height: 600px;
        }

        .aside {
            grid-area: aside;
            height: 600px;
        }

        .booter {
            grid-area: booter;
            height: 80px;
        }

        .header, .menu, .aside, .booter {
            display: flex;
            justify-content: center;
            align-items: center;
            background: white;
            opacity: .8;
            border-radius: 10px;
        }
</style>
