FROM public.ecr.aws/gravitational/teleport-distroless:18.7.3

COPY teleport.yaml /etc/teleport.yaml

VOLUME ["/var/lib/teleport"]

EXPOSE 3025 3080

ENTRYPOINT ["/usr/local/bin/teleport"]
CMD ["start", "--config=/etc/teleport.yaml"]
