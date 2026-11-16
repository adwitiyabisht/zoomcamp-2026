FROM python:3.13.11-slim

WORKDIR /app

ENV PATH="/app/.venv/bin:$PATH"

COPY "pyproject.toml" "uv.lock" ".python-version" ./

RUN uv sync --locked

COPY pipeline.py pipeline.py

ENTRYPOINT ["uv", "run", "python", "pipeline.py" ]