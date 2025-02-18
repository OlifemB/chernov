<script>
    const data = {
        buttons: [{
            id: 'first-tab',
            'class': 'active',
            'data-bs-toggle': 'tab',
            'data-bs-target': '#first',
            'aria-controls': 'first',
            'aria-selected': true,
            tabindex: '-1',
            title: 'Оформление заказа в AVITO',
        }, {
            id: 'second-tab',
            'data-bs-toggle': 'tab',
            'data-bs-target': '#second',
            'aria-controls': 'second',
            'aria-selected': false,
            title: 'Варианты доставки AVITO',
        }, {
            id: 'third-tab',
            'data-bs-toggle': 'tab',
            'data-bs-target': '#third',
            'aria-controls': 'third',
            'aria-selected': false,
            title: 'Заполнение заявки на доставку',
        }, {
            id: 'four-tab',
            'data-bs-toggle': 'tab',
            'data-bs-target': '#four',
            'aria-controls': 'third',
            'aria-selected': false,
            title: 'Часто задаваемые вопросы',
        }]
    }

    const btnClass = 'browser-tab fs-8 position-relative overflow-hidden text-center shadow fw-semibold w-100 px-2 py-3 rounded-4 text-wrap border-0'

</script>

<div class="rounded container" role="tablist">
    <div class="row flex-wrap d-flex">
        {#each data.buttons as button}
            <div class="col-md-6 my-2">
                <button
                        id={button.id}
                        class={`${btnClass} ${button.class ? button.class : ''}`}
                        data-bs-toggle={button['data-bs-toggle'] ? button['data-bs-toggle']: "tab"}
                        data-bs-target={button['data-bs-target'] ? button['data-bs-target']: "#"}
                        aria-controls={button['aria-controls'] ?button['aria-controls']:''}
                        aria-selected={button['aria-selected']?button['aria-selected']:false}
                        type="button"
                        role="tab"
                        tabindex="-1"
                >
                    {button.title}
                </button>
            </div>
        {/each}
    </div>
</div>