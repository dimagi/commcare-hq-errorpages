# CommcareHQ Error Pages
This repo holds error pages that are served outside of django

## CSS
This is intentionally not a super repeatable process, these files should almost never need to be updated.
There are three css files
* style/bootstrap-style.css: Bootstrap 3 css
* style/style.css: public site css, compiled by:
  * In the main Commcare repo in apps/style/static/public/less `/opt/lessc/bin/lessc public-style.less > style.css`
* style/additional-style.css: Anything specific to this page, e.g. change link color on blue background

## Testing locally
run nginx w/ a site:
server {
    server_name localhost;
    location / {
        root <path to>/commcare-hq-errorpages/pages;
    }
}

