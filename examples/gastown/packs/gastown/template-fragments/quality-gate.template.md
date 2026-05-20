{{- define "quality-gate-guidance" -}}
{{- if .InstructionsFile }}
   Run the quality gates described in `{{ .InstructionsFile }}` at the repo root.
   If that file is missing or contains no gate commands, fall back to:
{{- end }}
   ```bash
   go test ./...             # or: make test
   golangci-lint run ./...   # or: make lint
   ```
{{- end -}}
