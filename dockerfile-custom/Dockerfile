# Step 1: Specify the base image
FROM alpine

# Step 2: Download and install dependencies
RUN apk add --update redis

# Step 3: Setup the startup command
CMD ["redis-server"]