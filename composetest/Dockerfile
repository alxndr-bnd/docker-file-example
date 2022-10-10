# syntax=docker/dockerfile:1
FROM node:12-alpine
RUN apk --no-cache add curl

RUN mkdir -p /scripts
WORKDIR /scripts
COPY Jira-backup.sh .
COPY api-token.sh .
RUN chmod +x Jira-backup.sh

ENTRYPOINT ["./Jira-backup.sh"]
