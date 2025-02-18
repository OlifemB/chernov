<script>
    const data = {
        title: 'Варианты доставки AVITO',
        subtitle: 'У AVITO есть варианты доставки сторонними службами. Получателя указываете в зависимости от курьерской доставки:',
        list: [{
            title: 'Почта России',
            content: [
                `<b>Адрес доставки:</b> Ростовская обл., г.Донецк, пр-кт Ленина, д. 3.`,
                `Доверенность: Необходимо создать электронную доверенность на <b>Воротынцеву Татьяну Александровну +7(928)116-71-42</b> в личном кабинете Почты России.`
            ]

        }, {
            title: 'DPD',
            content: [
                `<b>Адрес доставки:</b> ПВЗ DPD - Ростовская обл., г. Донецк, ул. М.Горького, д. 160.`,
                `<b>Код получения:</b> Необходимо указать код получения в DPD.`
            ]
        }, {
            title: 'Boxberry',
            content: [
                `<b>Адрес доставки:</b> ПВЗ Boxberry - Ростовская обл., г. Донецк, ул. М.Горького, д. 160.`,
                `<b>Код получения:</b> Необходимо указать код получения в Boxberry.`
            ]
        }, {
            title: 'Курьерская доставка',
            content: [
                `<b>Адрес доставки:</b> Ростовская обл., г. Донецк, 3 мкр., д. 1 (ПВЗ OZON)`,
                `<b>Получатель:</b> Указываете себя, дополнительным получателем указываете Воротынцева Татьяна Александровна, тел. +7 (928) 116-71-42`
            ]
        }, {
            title: 'Яндекс',
            content: [
                `<b>Адрес доставки:</b> Ростовская область, г. Донецк, пр-кт Мира, д. 142`,
                `<b>Код получения:</b> При заполнении формы необходимо указать код получения в Яндекс.`
            ]
        }, {
            title: 'CDEK',
            content: [
                `Если заказ оформлен на доставку через CDEK, то необходимо оформлять заявку по инструкции CDEK, на странице услуги CDEK.`,
                `<a href="https://ftekrf.ru/cdek.html" target="_blank" class="btn btn-primary mt-auto">
                    Перейти к инструкции CDEK
                 </a>`
            ]
        },]
    }
</script>

<div
        class="tab-pane py-3 fade-in "
        id="second"
        role="tabpanel"
        aria-labelledby="second-tab"
>
    <h2 class="step-title fs-md-3 fs-4 fw-bold mb-2 pb-2 text-center text-md-start ps-2">
        {data.title}
    </h2>

    <div class="step-description px-3 px-md-0">
        <p class="mb-2 text-center text-md-start ps-0 ps-md-2 fs-6 py-4">
            {data.subtitle}
        </p>

        <div class="step-description mb-3">
            <div class="row g-3">
                {#each data.list as card}
                    <div class="col-md-6">
                        <div class="card custom-card shadow d-flex justify-content-center position-relative mt-2 overflow-hidden rounded">
                            <div class="py-4 px-2 d-flex flex-column text-center gap-2">
                                <h4 class="card-title custom-card-title fw-semibold mb-2 mt-2 mt-md-0 mt-lg-0 mt-xl-0">
                                    {card.title}
                                </h4>

                                {#each card.content as content}
                                    <p class="px-lg-4 px-2 mb-1">{@html content}</p>
                                {/each}
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</div>