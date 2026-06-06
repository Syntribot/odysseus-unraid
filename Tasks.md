# Odysseus Unraid Community App — Tasks

## Phase 1: Repository setup

- [ ] Push this repo to a GitHub account
- [ ] In repo Settings → Actions → General: enable "Allow all actions"
- [ ] In repo Settings → Actions → General: set Workflow permissions to "Read and write permissions"
- [ ] Push to `main` to trigger `.github/workflows/docker-publish.yml`
- [ ] Verify the Action runs successfully and a GHCR package appears under the repo Packages section
- [ ] Make the GHCR package public: Packages → select package → Package settings → Change visibility to public

## Phase 2: GitHub Actions & Docker image

- [ ] In repo Settings → Actions → General: enable "Allow all actions"
- [ ] In repo Settings → Actions → General: set Workflow permissions to "Read and write permissions"
- [ ] Push to `main` to trigger `.github/workflows/docker-publish.yml`
- [ ] Verify the Action runs successfully and a GHCR package appears under repo → Packages
- [ ] Make the GHCR package public: Packages → select the package → Package settings → Change visibility to public

## Phase 3: Install on Unraid (Individual templates)

- [ ] Install Odysseus-ChromaDB companion container from CA
- [ ] Install Odysseus-SearXNG companion container from CA
- [ ] Install Odysseus-ntfy companion container from CA
- [ ] Install the main Odysseus app from CA
- [ ] Verify all four containers are running in Docker tab
- [ ] Check Odysseus logs for auto-generated admin password
- [ ] Log in at `http://<unraid-ip>:7000`
- [ ] Change the default admin password in Settings
- [ ] Configure LLM provider (Ollama, OpenAI, or local endpoint) in Settings

## Phase 3b: Install on Unraid (Compose stack — alternative)

- [ ] Install the **Docker Compose Manager** plugin from CA
- [ ] Docker → Compose → Add New Stack → name it "odysseus"
- [ ] Paste the content from `https://raw.githubusercontent.com/realitymolder/Odysseus-Unraid/main/docker-compose.yml`
- [ ] Click "Compose Up" to deploy all 4 containers at once

## Phase 4: Submit to Unraid Community Apps

- [ ] Visit https://ca.unraid.net/submit and read the guidelines
- [ ] Click "Start Submission" and sign in with your Unraid forum account
- [ ] Enter the repo URL: `https://github.com/realitymolder/Odysseus-Unraid`
- [ ] Run the validation scan and fix any issues
- [ ] Click "Submit" for moderator review
- [ ] Wait for moderator review and address any feedback

## Phase 5: Ongoing maintenance

- [ ] Optional: enable NVIDIA GPU passthrough (`--runtime=nvidia` + `NVIDIA_VISIBLE_DEVICES=all`)
- [ ] Update the Odysseus image by re-running the GH Action workflow on demand
- [ ] Keep `docker-compose.yml` in sync with upstream changes
