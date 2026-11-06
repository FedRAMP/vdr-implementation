# Validation Tools

Upload a completed JSON or CSV file. Your browser checks the file locally without uploading or saving its contents. If this validator does not work because your file is too large,
please use a command-line validator - any JSON Schema or CSV Schema validator will work.

The validator checks required answers, dates, statuses, duplicate or missing rules, and offering metadata. It cannot tell whether your implementation works or your explanation is adequate.

<div id="validator" class="validator">
  <label for="submission-file">JSON or CSV file</label>
  <input id="submission-file" type="file" accept=".json,.csv,application/json,text/csv">
  <div class="validator-row">
  <label for="format">File format</label>
  <select id="format"><option value="json">JSON</option><option value="csv">CSV</option></select>
  <label for="submission-text">File contents — you can also paste or edit here</label>
  <textarea id="submission-text" rows="12" spellcheck="false" aria-describedby="text-help"></textarea>
  <p id="text-help">The selected file stays on your device. Editing here does not change the original file.</p>
  <button id="run-validation" type="button">Validate</button>
  <p id="validation-summary" role="status" aria-live="polite">Choose a file or load an example to begin.</p>
  <ul id="validation-errors"></ul>
</div>

<noscript>Enable JavaScript to use the browser validator, or use the command-line instructions below.</noscript>
