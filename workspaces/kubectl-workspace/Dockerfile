FROM alnoda/codeserver-workspace:5.0

RUN wrk install kubectl==stable
RUN wrk install helm==v3.14.0
RUN wrk install k9s==v0.32.5
RUN wrk install kdash==0.6.0
RUN wrk install kubectx==0.9.5
RUN wrk install kubetail==1.6.20
RUN wrk install ktunnel==1.6.1
RUN wrk install kubefwd==1.22.5
RUN wrk install kubie==0.23.1
RUN wrk install kubescout==0.1.16
RUN wrk install ktop==0.3.7
RUN wrk install kubectl-doctor==0.3.1
RUN wrk install kubectl-tree==0.4.3
RUN wrk install kubespy==0.6.3
RUN wrk install kube-dump==1.1.2
RUN wrk install octant==v0.25.1
RUN wrk install kubescape==latest
RUN wrk install kube-shell==latest
RUN wrk install krew==v0.4.4
RUN wrk install kube-hunter==0.6.8
RUN wrk install argocd-cli==v2.12.1
RUN wrk install trivy==0.54.1
RUN wrk install helmfile==0.167.1
RUN wrk install kubectl-aliases==latest
RUN wrk install velero-cli==1.14.0

# Install additional codeserver extensions 
RUN echo "------------------------------------------------------ extensions" \
    && code-server --install-extension  ms-kubernetes-tools.vscode-kubernetes-tools \
    && code-server --install-extension  ipedrazas.kubernetes-snippets

# Gonfigure Alnoda workspace
COPY --chown=abc:abc workspace /tmp/workspace
RUN wrk build /tmp/workspace && rm -rf /tmp/workspace
