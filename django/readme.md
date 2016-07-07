## Django

### Build absolute URL for twitter / fb meta tags
```html
<meta name="twitter:image" content="{% if request.is_secure %}https{% else %}http{% endif %}://{{ request.get_host }}{% static 'path/to/img.format' %}">
```
