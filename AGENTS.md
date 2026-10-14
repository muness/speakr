# Upstream first

Before patching Speakr behavior, check upstream issues, releases, and existing settings. Update this checkout to the latest upstream release and deploy that update first when authorized, then verify whether the issue remains. Add a custom patch only if the current upstream version and its settings do not resolve it. Preserve local integration changes and deployment configuration; back up the live database before deploying updates that migrate it.

Source deployments require the current upstream build steps. Run `bash scripts/build_css.sh` before serving the app: the generated `static/css/tailwind.css` is not tracked in Git. Verify the live browser after upgrading, including hidden modals and sidebar date sorting.
