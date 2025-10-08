# # Stage 1: Builder
# FROM python:3.11-slim
# WORKDIR /app
# COPY requirements.txt .
# RUN pip install  --no-cache-dir -r requirements.txt

# # # Stage 2: Runtime
# # FROM python:3.11-slim
# # WORKDIR /app
# # COPY --from=builder /root/.local /root/.local
# # ENV PATH=/root/.local/bin:$PATH
# COPY . .
# CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]


FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY main.py .

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
