# Week 04: Fetch and Format JSON

This small Coding 101 website demonstrates how to load local JSON files with
JavaScript and display their contents in HTML tables. It also contains a
navigation bug for you to investigate and fix with GitHub Copilot.

## Run the website

The pages use `fetch()` to load JSON, so open them through a local web server
instead of opening the HTML files directly from your computer.

1. Open a terminal in this project folder.
2. Start a server:

	 ```bash
	 python3 -m http.server 8000
	 ```

3. Visit [http://localhost:8000](http://localhost:8000) in your browser.
4. Stop the server with `Ctrl+C` when you are finished.

## Explore the pages

- `index.html` is the home page.
- `formatLeaveData.html` loads `leave.json`.
- `formatPeopleData.html` loads the people list from `people.json`.
- `formatWeekdayData.html` loads `weekday.json`.
- Each page's JavaScript file fetches data, builds a table, and displays
	loading or error text in the page.

## Bug-fix activity: weekday navigation

One of the website's navigation links does not open its page. Reproduce the
problem by using the Weekday link from the home page. Your goal is to find and
fix the cause, not just hide or remove the link.

### Work with GitHub Copilot

Use Copilot Chat in VS Code. Keep the relevant HTML files open or attach them
to your prompt with `#index.html` and `#formatWeekdayData.html`.

1. **Ask for a diagnosis, not a patch:**

	 > The Weekday link on this website does not open the weekday page. Compare
	 > the link with the actual files in this project. Explain the likely cause
	 > and point me to the exact file and line to inspect. Do not edit anything
	 > yet.

2. **Check Copilot's reasoning.** Compare the link target with the actual
	 filename in the Explorer. Remember that filenames and paths must match,
	 including capitalization.

3. **Ask for a minimal fix:**

	 > Make the smallest change needed so the Weekday navigation link opens the
	 > existing weekday page. Do not change unrelated page content. Explain
	 > what you changed.

4. **Review the proposed change.** Make sure it points to the existing page
	 and does not alter unrelated links. Accept the edit only if it matches the
	 intended behavior.

5. **Test it in the browser.** Reload the home page, click the Weekday link,
	 and confirm the weekday table appears. Also check that Home, Leave, and
	 People navigation still work.

### What counts as done

- The Weekday link opens the weekday page without a not-found error.
- The weekday page displays data from `weekday.json`.
- The other navigation links still work.
- You can explain the mismatch Copilot helped you find and how you verified
	the fix.

## Tips for using Copilot

- Give Copilot the observed behavior, the expected behavior, and relevant
	filenames. Specific context makes its diagnosis easier to verify.
- Ask it to explain the cause before asking it to edit code.
- Review every diff. Copilot can suggest changes outside the scope of the
	task, and you are responsible for deciding whether they belong.
- If the page still fails, open the browser developer tools and check the
	Console and Network tabs for the requested URL and any errors.
