FROM microsoft/dotnet:2.1-runtime-deps
# Add Tini
ENV TINI_VERSION v0.17.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /tini
RUN groupadd -r siggame && useradd -r -g siggame siggame \
    && apt-get update \
    && apt-get install libunwind8 \
    && mkdir /client && chown -R siggame:siggame /client \
    && chmod +x /tini
WORKDIR /client

ENTRYPOINT ["/tini", "--", "./joueur-cs"]
