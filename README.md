# EDIT ZONE BD — Render
1. Upload this project to GitHub.
2. Render → New → Web Service → connect the repo.
3. Select Docker deployment (Dockerfile is included).
4. Add environment variable `ADMIN_PASSWORD` = `64713`.
5. Deploy.
For permanent uploads/database, attach a Render Persistent Disk and set `DATA_DIR=/var/data`, mounted at `/var/data`. Without persistent storage, uploaded files/database can be lost when the service is recreated. The app blocks common server-side script extensions in uploads and limits uploads to 50 MB.
