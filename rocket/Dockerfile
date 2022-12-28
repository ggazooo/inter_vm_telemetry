FROM erichough/nfs-server

COPY exports.txt /etc/exports
COPY . .

RUN adduser --disabled-password --gecos "" --uid 7689 test_user
RUN mkdir --parents /nfs/test_share
RUN chown test_user:test_user /var/lib/nfs
RUN chown test_user:test_user /nfs/test_share

RUN chmod +x hello_rocket.sh
RUN ./hello_rocket.sh

CMD ["tail", "-f", "/dev/null"]

