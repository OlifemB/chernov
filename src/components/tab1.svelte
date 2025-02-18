<script>
    const data = {
        title: 'Оформление заказа в AVITO',
        subtitle: 'Для того, чтобы оформить заказ на Avito, необходимо:',
        list: [{
            icon: 'bi bi-person-plus-fill me-0 me-md-1',
            title: 'Регистрация на AVITO: ',
            text: `Необходимо зарегистрироваться на <a class="d-inline" target = "_blank" href = "https://www.avito.ru/" >сайте</a>, либо в приложении AVITO. При регистрации обязательно указывайте собственные контактные данные (ФИО, номер телефона, адрес электронной почты).`
        }, {
            icon: 'bi bi-shop-window me-0 me-md-1',
            title: 'Выбор товаров:',
            text: 'Выбираете товар, связываетесь с продавцом и оформляете Авито-доставку'
        }, {
            icon: 'bi bi-cart-fill me-0 me-md-1',
            title: 'Способ доставки: ',
            text: 'выбираете один из способов и адрес доставки. Информация о способах доставки в разделе "Варианты доставки AVITO"'
        }, {
            icon: 'bi bi-credit-card-fill me-0 me-md-1',
            title: 'Оплата заказа:',
            text: 'самостоятельно оплачиваете заказ и отслеживаете.'
        }],
        alert: 'Внимание! Авито-доставка является высоко рисковой сделкой, поскольку продавцы могут оказаться мошенниками и отправить другой товар или отличающегося качества. При получении заказа явно отличающего от заявленного Вами - наш менеджер согласует дальнейшие действия. Если визуально нет возможности определить соответствие – все риски ложатся на покупателя.'
    }
</script>

<div
        class="tab-pane py-3 fade-in active show"
        id="first"
        role="tabpanel"
        aria-labelledby="first-tab"
>
    <h2 class="step-title fs-md-3 fs-4 fw-bold mb-2 pb-2 text-center text-md-start ps-2">
        {data.title}
    </h2>

    <div class="step-description px-3 px-md-0">
        <p class="mb-2 text-center text-md-start ps-0 ps-md-2 fs-7 py-4">
            {data.subtitle}
        </p>

        <ul class="icon-list d-flex flex-column align-items-center justify-content-center d-md-inline-block text-center text-md-start list-unstyled ps-0 ps-md-3 gap-4">
            {#each data.list as item}

                <li class="mb-3 d-flex flex-row align-items-start justify-content-start gap-2">
                    <i class={item.icon + ' d-none d-md-block'} style="width:18px"></i>

                    <div class="d-flex flex-column">
                        <div class="fw-bold fs-6">
                            <i class={item.icon + ' d-inline-block d-md-none'} style="width:18px"></i>
                            {item.title}
                        </div>
                        <p class="fs-7">
                            {@html item.text}
                        </p>
                    </div>
                </li>
            {/each}
        </ul>

        <div class="alert alert-danger p-3 rounded">
            <i class="bi bi-shield-fill-exclamation me-2 fs-7"></i>
            {data.alert}
        </div>
    </div>

</div>