# Source scan archive

[`registro.jsonl`](registro.jsonl) is the shared URL register for project research. Each line is a JSON object with one URL, its aggregate status, and the observations that support it. The register is independent of the feature workbook and includes pages that did not yield a feature.

| Status | Meaning |
| --- | --- |
| `scanned` | The page was examined for the scope stated in an observation. |
| `retrieved` | The page was accessed. The evidence does not establish a completed content scan. |
| `unavailable` | An access attempt failed and no successful access is recorded. |
| `discovered` | The URL was identified and has no recorded access attempt yet. |

## Research workflow

1. Look up the URL before opening it. Use the final verified URL and preserve any aliases or redirects in the observations. Remove tracking parameters, retain query parameters that select content or pagination, and record a relevant heading fragment separately. Use the English Microsoft Learn URL as the canonical key when the same article was accessed through a localized URL.
2. Reuse notes and local extracts for URLs already retrieved or scanned. Reopen a previously accessed page only on explicit user request. If the original access left too little evidence for further analysis, record the gap. A failed attempt remains visible and can be retried when needed.
3. Log URLs individually as they are discovered or processed. Include the date, the scope, the outcome, the originating index or article when known, and a durable checkpoint or evidence reference. Keep earlier observations when the outcome changes.
4. Follow the same process for paginated indexes, individual articles, and linked references. An index scan does not mark its articles as scanned. A scan for release-note links does not establish full feature verification. Mark archive coverage complete in the checkpoint only when the entire relevant archive has been accounted for.

## Historical import

The initial register draws on checkpoints, the Microsoft Learn release-note index, the Version Manager comparison, and local release-note and date-audit evidence. A historical entry includes a date only when the available evidence identifies it. The checkpoint still holds aggregate coverage for older batches whose individual URLs were not retained. Those batches do not imply a successful scan for any unlisted URL.
