---
permalink: /Presentations/
title: "Presentations"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

{% assign presentations = site.data.presentations | sort: 'year' | reverse %}
{% assign presentationsPerPage = 3 %}
{% assign totalPages = presentations.size | divided_by: presentationsPerPage | plus: 1 %}

{% for page in (1..totalPages) %}
  {% capture currentPage %}{{ page }}{% endcapture %}
  {% assign presentationsOnPage = presentations | slice: (page | minus: 1) | times: presentationsPerPage, presentationsPerPage %}
  
  {% if presentationsOnPage.size > 0 %}
    ## 演示 - 第 {{ currentPage }} 页

    {% for presentation in presentationsOnPage %}
      {% assign year = presentation.year %}
      {% if forloop.first or year != presentationsOnPage[forloop.index0 | minus: 1].year %}
        ### {{ year }}
      {% endif %}
      {{ forloop.index }}. **{{ presentation.presenter }}**. {{ presentation.title }} – {{ presentation.event }}, {{ presentation.date }}. **\[{{ presentation.type }}\]**
    {% endfor %}
  {% endif %}
{% endfor %}

Presenter highlighted in **bold**

## 2023
1. **Xu Gao**.  Epidemiology of air pollution and human aging: preliminary findings – The 7th Conference on Environmental Health Risks and Prevention and Control of New Environmental Pollutants, Zhengzhou, China, May 2023. **\[Oral\]** 
2. **Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study – The 7th Conference on Environmental Health Risks and Prevention and Control of New Environmental Pollutants, Zhengzhou, China, May 2023. **\[Oral\]** 
3. **Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study – The 7th Asian Congress on Environmental Mutagens, Qingdao, China, May 2023. **\[Oral\]** 

## 2022
1. **Xu Gao**.  Data processing of cardiometabolic multimorbidity and study findings – The 33rd Great Wall International Congress of Cardiology / Asia Heart Society Congress 2022, Online Virtual, October 2022. **\[Oral\]** 
2. **Xu Gao**.  Role of sleep quality in the acceleration of biological aging and its potential for preventive interaction on air pollution insults: Findings from the UK Biobank cohort– International Society of Environmental Epidemiology 2022 Conference, Athence, Greece, September 2022. **\[Oral\]** 
3. **Xu Gao**.  Preliminary findings on the associations of air pollution with elderly health and relevant interventions – Environment and Health Academic Conference 2021-2022, Lanzhou, China, July 2022. **\[Oral\]** 

## 2021
1. **Xu Gao**.  Short-term air pollution, cognitive performance and nonsteroidal anti-inflammatory drug use in the Veterans Affairs Normative Aging Study– China 27th Conference on Atmospheric Environment Science and Technology, Online Virtual, November 2021. **\[Oral\]** 
2. **Xu Gao**.  Epidemiological findings on environmental aging – China Conference on Environment and Health 2021, Chengdu, China, October 2021. **\[Keynote speaker & Session Chair\]** 
3. **Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study in young healthy adults – Beijing Conference and Exhibition on Instrumental Analysis, Beijing, China, September 2021. **\[Keynote speaker\]** 
4. **Xu Gao**.   Environmental risk factors for chronic kidney disease – International Society of Environmental Epidemiology 2021 Conference, Online Virtual, August 2021. **\[Session Chair\]** 
5. **Xu Gao**.  Short-term exposure to PM2.5 and epigenetic aging: a quasi-experimental study – International Society of Environmental Epidemiology 2021 Conference, Online Virtual, August 2021. **\[Session Chair\]** 

Updated 08/01/2023
