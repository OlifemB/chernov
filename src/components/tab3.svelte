<script>
    const data = {
        title: 'Заполнение заявки доставки',
        subtitle: 'При поступлении заказа на выбранный Вами пункт выдачи, нужно заполнить заявку:',
        list: [{
            icon: 'bi bi-buildings-fill me-0 me-md-1',
            title: 'Город получателя:',
            text: 'Выберите один из перечисленных городов, где находиться FTEK.'
        }, {
            icon: 'bi bi-shop-window me-0 me-md-1',
            title: 'Пункт выдачи:',
            text: 'Выберите ПВЗ FTEK.'
        }, {
            icon: 'bi bi-person-fill me-0 me-md-1',
            title: 'ФИО получателя:',
            text: 'Указываете актуальные данные получателя.'
        }, {
            icon: 'bi bi-telephone-fill me-0 me-md-1',
            title: 'Номер телефона получателя:',
            text: 'Указываете актуальные данные получателя'
        }, {
            icon: 'bi bi-envelope-at me-0 me-md-1',
            title: 'Электронная почта: ',
            text: 'Указываете рабочую почту, для отслеживания заказа'
        }, {
            icon: 'bi bi-123 me-0 me-md-1',
            title: 'Номер заказа:',
            text: 'Необходимо указать номер заказа Avito'
        }, {
            icon: 'bi bi-123 me-0 me-md-1',
            title: 'Код получения:',
            text: 'Указать код получение заказа Avito'
        }, {
            icon: 'bi bi-qr-code me-0 me-md-1',
            title: 'Штрихкод, QR-код:',
            text: 'Загрузите скриншот со штрихкодом/QR-кодом с вашего заказа в Avito.'
        }, {
            icon: 'bi bi-camera-fill me-0 me-md-1',
            title: 'Скриншоты товаров:',
            text: 'Загрузите скриншоты получаемых товаров.'
        }, {
            icon: 'bi rouble me-0 me-md-1 h-100 d-block',
            title: 'Объявленная стоимость:',
            text: 'Укажите общую стоимость получаемых товаров (в рублях).'
        }, {
            icon: 'bi bi-chat-left-dots-fill me-0 me-md-1',
            title: 'Комментарий к заказу:',
            text: 'Укажите при необходимости дополнительные комментарии к заказу.'
        }, {
            icon: 'bi bi-check2-circle me-0 me-md-1',
            title: 'Условия:',
            text: 'Ознакомьтесь и примите условия оферты и обработки персональных данных.'
        }, {
            icon: 'bi bi-send-check-fill me-0 me-md-1',
            title: 'Оформление:',
            text: 'Нажмите "Оформить заказ".'
        },]
    }
</script>

<div
        class="tab-pane py-3 fade-in"
        id="third"
        role="tabpanel"
        aria-labelledby="third-tab"
>
    <h2 class="step-title fs-md-3 fs-4 fw-bold mb-2 pb-2 text-center text-md-start ps-2 ">
        {data.title}
    </h2>

    <div class="step-description px-3 px-md-0">
        <p class="mb-2 text-center text-md-start ps-0 ps-md-2 fs-7 py-4">
            {data.subtitle}
        </p>

        <ul class="icon-list mb-0 d-flex flex-column align-items-center justify-content-center d-md-inline-block text-center text-md-start list-unstyled ps-0 ps-md-3 gap-3">
            {#each data.list as item}
                <li class="mb-3 d-flex flex-row align-items-start justify-content-start fs-7">
                    <i class={`${item.icon} h-max d-none d-md-block`}></i>

                    <div class="d-flex flex-column">
                        <div class="fw-bold fs-6">
                            <i class={item.icon + ' d-inline-block d-md-none'} style="width:18px"></i>
                            {item.title}
                        </div>

                        <div class="py-0 my-0 fs-7">
                            {item.text}
                        </div>
                    </div>
                </li>
            {/each}
        </ul>
    </div>
</div>