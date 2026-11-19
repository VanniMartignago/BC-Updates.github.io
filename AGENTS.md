# Project instructions

For each feature update, follow the official references cited by approved complementary sources and verify that they substantiate the specific feature before recording them. For each approved blog, review its entire Business Central feature coverage, including every page of relevant paginated archives and relevant posts found through other site indexes. Compare eligible features with the current workbook, verify the official references cited in each article, and record which pages were reviewed or could not be accessed. Mark coverage complete only after the entire relevant archive has been reviewed.

Title each update pull request `Added features XX, modified YY on DD-MM-YYYY`. After committing, show the user separate lists of added and modified feature titles. Wait for explicit approval before merging into main. After the merge, synchronize the local main with GitHub and verify both point to the same commit.

If developing AL code in VS Code, follow `.github/copilot-istructions.md` when present.

The project maintains an English-language blog documenting Microsoft Dynamics 365 Business Central features from version 13 through the current release. `Business_Central_Updates.xlsx` is the primary database; generate `Business_Central_Updates.json` from the Excel data. The workbook's existing structure and contents are a starting point and may evolve.

For each feature update, start from the latest existing workbook version and preserve all previous workbook files unchanged. Use `Business_Central_Updates.xlsx` as the initial baseline. Save the updated database as the next sequential version, beginning with `Business_Central_Updates_V1.xlsx`, then `Business_Central_Updates_V2.xlsx`, and so on. Carry forward the preceding version's data, incorporating verified additions and updates. Regenerate `Business_Central_Updates.json` from the latest Excel version after each update.

After the new sequential workbook and its JSON have been updated and verified, move all older numbered workbooks and their inspection sidecars from the project root into `archivio`, without changing their contents. Keep only the newest numbered workbook in the project root. When selecting the current workbook, counting current data files, or searching current feature entries, ignore every file in `archivio`; use the newest numbered workbook in the root as the current database.

The `archivio` folder contains historical numbered workbooks and their inspection sidecars. Ignore this folder when selecting the latest current workbook, counting current data files, or searching for current feature entries. Keep the newest numbered workbook in the project root.

After generating and verifying the latest workbook and `Business_Central_Updates.json`, update the project's GitHub repository with those files using its supported workflow. Verify the resulting commit, pull request, or deployment before reporting completion. If GitHub access or a connected repository is unavailable, keep the verified files ready, record the GitHub update as incomplete, and resume when access is available.

Research and update features in chronological order, starting with version 13 and proceeding toward current releases. Verify and record the actual minor release for each feature where evidence is available; do not equate an update's existence with the introduction of a particular feature.

For the Microsoft Learn `whatsnew-update-{major}-{minor}` release-note series, check versions in order from 15.0 through 29.1: minor versions 0 through 5 for each major from 15 to 28, and 29.0 through 29.1. Some pages may be unavailable or follow a different naming convention; verify each URL and use other approved Microsoft sources where necessary. For version 13 and 14, use the approved historical documentation and update archives. Extend the release-note search as new versions are published.

For each feature maintain major version, full minor version, release wave, Microsoft product area, country/region for country-specific localized functionality, title, description, preview date, actual or planned general availability date, SaaS availability, on-premises availability, and a primary source link. Do not include a secondary source link column. Verify product areas against Microsoft's published classifications and only record countries or regions supported by evidence; leave the country/region field empty for general or unverified applicability. Write blog-facing data in English. Before adding or updating an area, compare it with all existing Product area values using case-insensitive, whitespace- and punctuation-insensitive matching, and check singular/plural and clearly equivalent wording. Reuse one canonical label for equivalent areas (prefer the latest verified Microsoft classification spelling, otherwise the established spelling used by the majority of existing rows); update existing rows when needed. Keep genuinely distinct product areas separate, even when their names are related, and never fill an area that is unknown. Use Yes/No for availability only when supported by evidence; leave unknown information unverified rather than guessing.

When a feature has a specified country or region and Microsoft does not identify a more precise product area, use `Country/region` as its product area. Retain a more precise officially documented product area when available.

Maintain a separate `Official documentation` link for detailed functional guidance from `https://learn.microsoft.com/en-us/dynamics365/business-central/`, in addition to the primary release source. Populate it only when a relevant Microsoft page has been verified; leave it empty when detailed documentation has not been found.

Maintain a separate `Blog source` link for a non-official blog article only when that article details the specific feature and focuses exclusively or predominantly on it. Do not link generic release roundups or articles that only mention the feature briefly. A blog-only discovery may be added with the primary source and Official documentation fields left empty; populate those official links later only after verifying relevant Microsoft sources.

Write each feature description as a clear English synthesis of relevant information found in approved primary and secondary sources. Explain the feature's purpose, what it does, and the practical context needed to understand it; include relevant limitations or prerequisites when supported by the sources. Prefer official documentation when sources conflict and do not invent details. Expand existing descriptions during verification when they do not adequately explain the feature.

At each update, propose newly discovered sources for documenting versions 13 through the current release before adding them as primary sources; obtain the user's approval before treating a new source as primary. Prefer a specific official Microsoft page as the primary source whenever available. Use secondary sources to enrich the feature description. When only a secondary source documents a feature, leave the primary source field empty. On subsequent updates, search for official documentation, add its link when found, and update the title and description as appropriate. Check existing entries for obsolete details and duplicates before adding or changing features; consolidate confirmed duplicates without conflating distinct features or version-specific enhancements. Distinguish planned, preview, and generally available features, and confirm planned dates against newer evidence. Regenerate the JSON from the updated Excel database.

The requested maintenance cadence is every Saturday. Check previously approved sources and follow the versioning and verification rules above. Propose any newly discovered non-Microsoft source for the user's confirmation before adding it as a project source; do not add or rely on it as an approved source until confirmed. In an unattended run, record proposed sources for review and continue independent work using approved sources.

If scanning all sources is expected to take more than 30 minutes, or if it reaches 30 minutes with sources still pending, divide the feature update into sessions. At the end of each session, summarize the sources reviewed, the work completed, and the next section to review, then ask the user for explicit confirmation before starting that section. This pause also applies to unattended runs. Resume from the recorded checkpoint after confirmation.

## Approved official Microsoft sources

- [Microsoft Learn MCP server](https://learn.microsoft.com/api/mcp): use its search and document retrieval tools to consult official Microsoft documentation when more efficient than web browsing. Cite the underlying documentation page as the feature source, not the MCP endpoint. Use other approved sources when the MCP does not provide sufficient coverage.
- [Business Central documentation](https://learn.microsoft.com/en-us/dynamics365/business-central/) and [product news](https://learn.microsoft.com/it-it/dynamics365/business-central/product-news): product documentation and released updates.
- The [verified Microsoft Learn update release notes](Microsoft_Learn_Release_Notes.md) and all other available official pages matching `https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/whatsnew/whatsnew-update-{major}-{minor}` are approved primary sources. Check for newly published pages when updating. Verify each page exists and check its feature status and any version-independent service-feature notes before assigning an introduction version.
- [Microsoft 365 roadmap](https://www.microsoft.com/it-it/microsoft-365/roadmap?filters=%5B%22Dynamics+365+Business+Central%22%5D#Roadmap): planned features; dates and scope can change.
- [Historical release plans](https://learn.microsoft.com/en-us/previous-versions/dynamics365/release-plan/2025wave2/) and other Microsoft release-plan archives: historical features and planned dates.
- [Microsoft Support Business Central updates](https://support.microsoft.com/en-us/servicing/dynamics/business-central/released-updates-for-microsoft-dynamics-365-business-central-2026-release-wave-1): update dates, builds, fixes, and regulatory changes. Consult the page for the relevant version; a cumulative update entry is not automatically a new feature.
- [Official Dynamics 365 Business Central blog](https://www.microsoft.com/en-us/dynamics-365/blog/product/dynamics-365-business-central/?sort-by=newest-oldest): announcements and context; corroborate availability and dates with product documentation when possible.
- [Microsoft BCApps releases](https://github.com/microsoft/BCApps/releases): application and technical changes; a changelog entry alone does not establish general availability.
- [Official Business Central LinkedIn posts](https://www.linkedin.com/company/microsoft-dynamics-365-business-central/posts/?feedView=all): announcements and leads for further verification.

## Complementary sources

- [Foxer — Business Central release updates](https://bc.foxer.pl/en/).
- [Yun Zhu — Dynamics 365 Lab, Business Central archive](https://yzhums.com/category/dynamics365/dynamics365businesscentral/).
- [Stefano Demiliani](https://demiliani.com/).
- [Version Manager](https://blog.versionmanager.dk/).
- [ArvyDev — Business Central release updates](https://arvydev.com/blog/business-central-2026-wave-2-whats-new/).
- [Daxly — Business Central release updates](https://www.daxly.io/blog/whats-coming-business-central-2026-wave-2/).
- [RS Business Central Blog](https://blogbcrs.wordpress.com/).
- [Business Central Musings](https://svirlan.com/mvp-year-in-review-2026/).
- [Rand Group — Business Central release updates](https://www.randgroup.com/insights/microsoft/dynamics-365/business-central/key-features-and-updates-in-the-2025-release-wave-1-of-business-central/).
- [Stuart Hardman — Business Central release updates on LinkedIn](https://www.linkedin.com/posts/stuart-hardman_businesscentral-msdyn365bc-erp-activity-7448309075483873280-bA78).
- [Kennie Nybo Pontoppidan — Business Central release videos on LinkedIn](https://www.linkedin.com/posts/kennie_msdyn365bc-activity-7445108586155925505-c7nA).

Use these non-official sources for additional detail and examples; prefer Microsoft documentation when available.
