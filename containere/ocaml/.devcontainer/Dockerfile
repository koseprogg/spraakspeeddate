FROM ocaml/opam:debian-ocaml-5.0

RUN opam switch create 5.0.0
RUN eval $(opam env)
RUN opam install -y ocaml-lsp-server ocamlformat

# Add opam binaries to PATH
ENV PATH="/home/opam/.opam/5.0.0/bin:${PATH}"

WORKDIR /workspace