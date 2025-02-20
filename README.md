# Dockerfile Best Practices
This example demonstrates issues that can arise from insufficiently specific Dockerfile instructions and provides a solution for improved reliability and maintainability. The original Dockerfile uses a generic base image, lacks explicit WORKDIR, and uses a simple CMD which is not as robust as it can be.

**Bug:** The `ubuntu:latest` image is not specific and can lead to unpredictable behavior depending on the system's updates. The lack of `WORKDIR` affects the file paths. The `CMD` should be more error resilient.

**Solution:** This issue is fixed by specifying a more specific Ubuntu version, declaring `WORKDIR`, and adding error handling to the `CMD` instruction.