---
permalink: /Presentations/
title: "Presentations"
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

Presenter highlighted in **bold**

<div id="presentations-container">
  <!-- Content will be dynamically added here -->
</div>

<script>
  // Define the presentations data
  const presentations = [
    {
      year: 2023,
      presentations: [
        "**Xu Gao**.  Epidemiology of air pollution and human aging: preliminary findings – The 7th Conference on Environmental Health Risks and Prevention and Control of New Environmental Pollutants, Zhengzhou, China, May 2023. **[Oral]**",
        "**Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study – The 7th Conference on Environmental Health Risks and Prevention and Control of New Environmental Pollutants, Zhengzhou, China, May 2023. **[Oral]**",
        "**Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study – The 7th Asian Congress on Environmental Mutagens, Qingdao, China, May 2023. **[Oral]**"
      ]
    },
    {
      year: 2022,
      presentations: [
        "**Xu Gao**.  Data processing of cardiometabolic multimorbidity and study findings – The 33rd Great Wall International Congress of Cardiology / Asia Heart Society Congress 2022, Online Virtual, October 2022. **[Oral]**",
        "**Xu Gao**.  Role of sleep quality in the acceleration of biological aging and its potential for preventive interaction on air pollution insults: Findings from the UK Biobank cohort– International Society of Environmental Epidemiology 2022 Conference, Athence, Greece, September 2022. **[Oral]**",
        "**Xu Gao**.  Preliminary findings on the associations of air pollution with elderly health and relevant interventions – Environment and Health Academic Conference 2021-2022, Lanzhou, China, July 2022. **[Oral]**"
      ]
    },
    {
      year: 2021,
      presentations: [
        "**Xu Gao**.  Short-term air pollution, cognitive performance and nonsteroidal anti-inflammatory drug use in the Veterans Affairs Normative Aging Study– China 27th Conference on Atmospheric Environment Science and Technology, Online Virtual, November 2021. **[Oral]**",
        "**Xu Gao**.  Epidemiological findings on environmental aging – China Conference on Environment and Health 2021, Chengdu, China, October 2021. **[Keynote speaker & Session Chair]**",
        "**Xu Gao**.  Short-term PM2.5 exposure and epigenetic aging: a quasi-experimental study in young healthy adults – Beijing Conference and Exhibition on Instrumental Analysis, Beijing, China, September 2021. **[Keynote speaker]**",
        "**Xu Gao**.  Environmental risk factors for chronic kidney disease – International Society of Environmental Epidemiology 2021 Conference, Online Virtual, August 2021. **[Session Chair]**",
        "**Xu Gao**.  Short-term exposure to PM2.5 and epigenetic aging: a quasi-experimental study – International Society of Environmental Epidemiology 2021 Conference, Online Virtual, August 2021. **[Session Chair]**"
      ]
    }
  ];

  // Function to generate HTML for presentations
  function generatePresentationsHTML(year, presentations) {
    let html = `<h2>${year}</h2>`;
    presentations.forEach(presentation => {
      html += `<p>${presentation}</p>`;
    });
    return html;
  }

  // Function to display presentations based on current page
  function displayPresentations(page) {
    const presentationsPerPage = 1;
    const startIndex = (page - 1) * presentationsPerPage;
    const endIndex = startIndex + presentationsPerPage;
    
    let html = '';
    for (let i = startIndex; i < endIndex && i < presentations.length; i++) {
      html += generatePresentationsHTML(presentations[i].year, presentations[i].presentations);
    }
    
    document.getElementById('presentations-container').innerHTML = html;
  }

  // Initial page to display
  let currentPage = 1;
  displayPresentations(currentPage);

  // Function to go to the next page
  function nextPage() {
    currentPage++;
    displayPresentations(currentPage);
    window.scrollTo(0, 0); // Scroll to top after changing page
  }

  // Add event listener to next page button
  document.getElementById('next-page-button').addEventListener('click', nextPage);
</script>

<!-- Next Page Button -->
<button id="next-page-button">Next Page</button>
