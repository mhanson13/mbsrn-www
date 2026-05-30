# mbsrn-managed-manifest:site_repo_template_v1
# Managed site runtime image build contract.
# This image is built from generated site content in the target repo.
# content_identity: mhanson13/mbsrn-www
FROM caddy:2.8-alpine
WORKDIR /srv
COPY context/ /srv/
EXPOSE 8080
CMD ["caddy", "file-server", "--root", "/srv", "--listen", ":8080"]
