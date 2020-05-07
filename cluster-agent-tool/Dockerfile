FROM alpine:3.11

RUN apk add --no-cache jq curl docker bash
RUN curl -o /bin/kubectl https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
RUN chmod 777 /bin/kubectl
ADD cluster-agent-tool.sh /bin/cluster-agent-tool.sh
RUN chmod +x /bin/cluster-agent-tool.sh
ENTRYPOINT ["cluster-agent-tool.sh"]