Usage:
Add the following code to product.twig

{% if special_active %}
    {% if special_start %}
        Promo start date: {{ special_start|date("d.m.Y H:i") }}
    {% endif %}

    {% if special_end %}
        Promo end date: {{ special_end|date("d.m.Y H:i") }}
    {% endif %}
{% endif %}

OR

{% if special_active %}
    <div class="product-special">
        🔥 Промоция активна
        {% if special_end %}
            до {{ special_end|date("d.m.Y H:i") }}
        {% endif %}
    </div>
{% endif %}