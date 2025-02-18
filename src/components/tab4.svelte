<script>
    const data = {
        title: 'Часто задаваемые вопросы',
        cards: [{
            title: 'Сколько стоит доставка?',
            text: 'тоимость доставки зависит от стоимости заказанных товаров. От 5 до 10 % процентов от стоимости, чем больше цена, тем меньше процент.'
        }, {
            title: 'Как отследить посылку?',
            text: 'Вы можете отследить статус посылки, воспользовавшись сервисом отслеживания на главной странице нашего сайта.'
        }, {
            title: 'Как долго хранится посылка?',
            text: 'Посылка хранится в пункте выдачи FTEK 7 календарных дней. По истечении этого срока наступает "платное хранение".'
        }, {
            title: 'Какой срок доставки?',
            text: '1-2 дня (с момента поступления заказа с Avito)'
        }, {
            title: 'Как оплатить доставку?',
            text: 'Оплата услуг доставки осуществляется получателем при получении в ПВЗ FTEK'
        }, {
            title: 'Как получать уведомления?',
            text: 'Вы будете получать уведомления о статусе заказа на указанную в заявке электронную почту'
        }]
    }
</script>

<div
        class="tab-pane py-3 fade-in "
        id="four"
        role="tabpanel"
        aria-labelledby="four-tab"
>
    <h2 class="step-title fs-md-3 fs-4 fw-bold mb-2 pb-2 text-center text-md-start ps-2">
        {data.title}
    </h2>

    <div class="container">
        <div class="row">
            {#each data.cards as card}
                <div class="col-md-6 my-2 my-md-3">
                    <div class="faq-item d-flex flex-column justify-content-center shadow custom-card card h-md-auto position-relative text-center p-4 rounded bg-white">
                        <h3 class="fs-5 fw-bolder mb-1 mt-4 mt-md-0">
                            {card.title}
                        </h3>

                        <p>
                            {card.text}
                        </p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</div>