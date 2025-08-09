# Summarisation Agent

This is a simple Lurawi agent that perform content summarisation using a (multi-modal) LLM.

## Prerequisite

```bash
pip install lurawi-agent
```

## Load Agent

```python
from lurawi.lurawi_agent import LurawiAgent

summary_agent = LurawiAgent(name="summary_agent", 
                                behaviour="summary_agent", workspace=".") 
# workspace is where summary_agent.json is located
```

## Run Agent

### Plain Text Input

```python
summary_agent.run_agent(summary_prompt="put your custom prompt", 
                            message="text content to be summarised")
```

### Plain Text Based File

```python
summary_agent.run_agent(summary_prompt="put your custom prompt",
                            text_file="/full/path/to/your/text/file")
```

### Image file

Image file including JPEG, PNG or any image format supported by PIL module

```python
summary_agent.run_agent(summary_prompt="put your custom prompt",
                            image_file="/full/path/to/your/image/file")
```

### PDF file

**NOTE** Your system must have [`poppler`](https://pdf2image.readthedocs.io/en/latest/installation.html#installing-poppler) module installed.

```python
summary_agent.run_agent(summary_prompt="put your custom prompt",
                            pdf_file="/full/path/to/your/pdf/file")
```
