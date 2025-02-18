<script>
    import Buttons from './buttons.svelte'
    import Header from './header.svelte'
    import Tab1 from './tab1.svelte'
    import Tab2 from './tab2.svelte'
    import Tab3 from './tab3.svelte'
    import Tab4 from './tab4.svelte'
</script>

<div class="content my-4">
    <div class="container">
        <Header/>
        <Buttons/>
        <div
                id="instructionTabsContent"
                class="tab-content mt-4 px-md-4 px-2 shadow bg-white rounded"
        >
            <Tab1/>
            <Tab2/>
            <Tab3/>
            <Tab4/>
        </div>
    </div>
</div>