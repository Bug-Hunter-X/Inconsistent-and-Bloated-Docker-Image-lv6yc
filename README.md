# Dockerfile Best Practices
This example demonstrates common pitfalls in Dockerfiles and how to fix them for consistent and efficient image builds.

**Problem:** The original Dockerfile uses `ubuntu:latest`, leading to potential inconsistencies across builds due to unpredictable base image updates.  It also fails to clean up temporary files, resulting in a bloated image.

**Solution:** The updated Dockerfile specifies a specific ubuntu version (`ubuntu:20.04`), utilizes `apt-get clean` to remove temporary packages and uses a `.dockerignore` file to exclude unnecessary files and directories from the build context.