## 📑 Paper Reviews by Category

### 🗣️ Text-to-Speech (TTS)
{% for review in site.reviews %}
  {% if review.category == "tts" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

### 🔊 Speech Enhancement
{% for review in site.reviews %}
  {% if review.category == "speech-enhancement" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

### 🎙️ Speech Processing
{% for review in site.reviews %}
  {% if review.category == "speech-processing" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

### 📖 NLP
{% for review in site.reviews %}
  {% if review.category == "nlp" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}