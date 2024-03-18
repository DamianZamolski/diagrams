sequenceDiagram

ba ->> badb: update status to uploading-to-policy
ba ->>+ pc: upload to policy
pc -->>- ba: ERROR: document already exists
ba ->> badb: update status to already-exists

participant badb as backend-archidoc-database
participant pc as policy-center
participant ba as backend-archidoc
