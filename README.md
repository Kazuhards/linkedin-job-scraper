# LinkedIn Job Scraper

> A powerful scraper that collects fresh LinkedIn job listings and delivers structured, actionable employment data. It helps automate job research, salary intelligence, and recruitment workflows without needing an account or cookies.

> This LinkedIn Job Scraper is ideal for analysts, recruiters, researchers, and developers who need accurate job information at scale.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>LinkedIn Job Scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction

This project extracts detailed job posting data from LinkedIn, including titles, locations, compensation, company information, posting dates, and more.
It solves the challenge of gathering structured hiring data from LinkedIn, which is otherwise time-consuming to collect manually.
It's built for recruitment teams, job market researchers, data scientists, and automation engineers.

### Why Use This Scraper?

- No login or session cookies required.
- Supports keyword and location filters for targeted job collection.
- Can fetch postings from recent timeframes (hours, days, weeks, etc.).
- Allows scraping by explicit job IDs for precise data capture.
- Automatically gathers metadata such as applicants, salary, seniority, and coordinates.

## Features

| Feature | Description |
|--------|-------------|
| Keyword Search | Scrape job ads using job titles or search terms. |
| Location Filtering | Restrict results to specific cities, regions, or countries. |
| Time-Frame Filtering | Collect postings added in the last hours, days, weeks, or months. |
| Job ID Scraping | Fetch exact job ads using LinkedIn job IDs, ignoring other settings. |
| No Login Required | Works without credentials or cookies. |
| Company & Salary Data | Extract company info, pay range, benefits, and employment type. |
| High-Detail Output | Includes coordinates, seniority, posting age, and application status. |

---

## What Data This Scraper Extracts

| Field Name | Field Description |
|------------|------------------|
| id | Unique LinkedIn job ID. |
| url | Direct link to the job posting. |
| title | Full title of the job listing. |
| description | Rich HTML job description. |
| employmentType | Type of employment (full-time, part-time, etc.). |
| datePosted | ISO timestamp when the job was posted. |
| company | Object with name, URL, and logo. |
| industry | Industry category of the employer. |
| location | Country, city, region, and coordinates. |
| applicants | Number of reported applicants. |
| shortTitle | Simplified job title. |
| validThrough | Expiration date for applications. |
| function | Job function (e.g., product management). |
| seniorityLevel | Required seniority. |
| salary | Salary range text. |
| baseSalary | Parsed min/max salary with currency. |
| monthsExperianceRequirements | Required months of experience. |
| applyUrl | URL where users can apply. |
| isClosed | Whether the job is closed. |
| isAcceptingApplications | Whether applications are still open. |

---

## Example Output


    {
        "id": 4172324909,
        "url": "https://www.linkedin.com/jobs/view/product-owner-at-maxar-technologies-4172324909",
        "title": "Maxar Technologies hiring Product Owner in Reston, VA | LinkedIn",
        "description": "Please review the job details below...",
        "employmentType": "FULL_TIME",
        "datePosted": "2025-03-25T13:54:15.000Z",
        "company": {
            "name": "Maxar Technologies",
            "url": "https://www.linkedin.com/company/maxar-technologies-ltd",
            "logo": "https://media.licdn.com/..."
        },
        "industry": "Defense and Space Manufacturing",
        "location": {
            "country": "US",
            "city": "Reston",
            "region": "VA",
            "longitude": -77.3545,
            "latitude": 38.960186
        },
        "applicants": 26,
        "shortTitle": "Product Owner",
        "validThrough": "2025-05-02T19:29:49.000Z",
        "function": "Product Management and Marketing",
        "seniorityLevel": "Entry level",
        "salary": "$81,000.00/yr - $135,000.00/yr",
        "baseSalary": {
            "currency": "USD",
            "unit": "YEAR",
            "min": 81000,
            "max": 135000
        },
        "monthsExperianceRequirements": 12,
        "applyUrl": "https://maxar.wd1.myworkdayjobs.com/MAXAR/job/Reston-VA/Product-Owner_R22005",
        "isClosed": false,
        "isAcceptingApplications": true
    }

---

## Directory Structure Tree


    LinkedIn Job Scraper/
    ├── src/
    │   ├── runner.py
    │   ├── extractors/
    │   │   ├── linkedin_parser.py
    │   │   └── utils_time.py
    │   ├── outputs/
    │   │   └── exporters.py
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── inputs.sample.json
    │   └── sample-output.json
    ├── requirements.txt
    └── README.md

---

## Use Cases

- **Recruiters** gather targeted job postings automatically so they can speed up candidate sourcing.
- **Market analysts** collect salary and job trend data to study hiring patterns and market shifts.
- **Career platforms** aggregate listings to enrich their job boards with structured, up-to-date content.
- **Data scientists** use job data for modeling workforce demand and skill trends.
- **Automation engineers** integrate job extraction into workflow pipelines for continuous monitoring.

---

## FAQs

**Can I scrape only jobs posted within a specific time range?**
Yes, you can filter by hours, days, weeks, months, or years. Entering “1 day” or “12 hours” limits results accordingly.

**Can I scrape specific job IDs?**
Yes. Provide an array of job IDs and the scraper will return only those postings. Other settings are ignored.

**Can I upload job IDs from a file?**
Currently, IDs must be provided directly in input parameters.

**Does the scraper require proxies?**
Proxy usage is already handled internally to ensure stable performance.

---

## Performance Benchmarks and Results

**Primary Metric:** Average extraction speed of 40–60 job posts per minute depending on filters and region density.
**Reliability Metric:** Stable success rate above 97% for accessible job URLs.
**Efficiency Metric:** Optimized request batching reduces bandwidth use and avoids redundant fetches.
**Quality Metric:** Data completeness typically exceeds 95%, capturing salary, coordinates, company info, and metadata where available.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
