# Workflow Components

## 1. Gmail Trigger

The workflow starts automatically when a new code-related email is received.

### Purpose

- Event-driven workflow activation
- Automated request handling
- Email monitoring

### Responsibilities

- Detect incoming emails
- Extract email content
- Pass code input into the workflow pipeline

## 2. Parallel LLM Processing

The workflow uses two independent AI chains running in parallel.

This improves:

- modularity
- scalability
- response quality

### 2.1 Code Summary Chain

This LLM chain generates a concise summary of the submitted code.

### Responsibilities

- Analyze functionality
- Explain logic flow
- Identify core operations
- Generate technical summaries

### Output

- functionality overview
- logic explanation
- summarized code description

### 2.2 Code Comments Chain

This LLM chain generates developer-friendly comments and readability suggestions.

### Responsibilities

- Generate code comments
- Explain important functions
- Improve readability
- Provide developer guidance

### Output

- suggested comments
- readability improvements
- explanation notes

## 3. Merge Node

The Merge node combines outputs from both parallel AI chains into a single workflow stream.

### Purpose

- synchronize AI outputs
- consolidate generated data
- prepare unified processing pipeline

### Responsibilities

- receive outputs from both LLM chains
- combine workflow streams
- pass merged results forward

## 4. Aggregate Node

The Aggregate node structures and organizes merged AI outputs.

### Purpose

- output organization
- structured data preparation
- unified response formatting
- after aggregate node i will have 1 node in my output

### Responsibilities

- organize generated content
- prepare consolidated AI data
- improve downstream formatting

## 5. Edit Fields Node

The Edit Fields node restructures and cleans the aggregated outputs before they are passed into the final LLM chain.

### Purpose

- organize merged AI outputs
- prepare structured prompt data
- improve final response formatting

### Responsibilities

- clean workflow data
- rename and structure fields
- prepare final LLM payload
- optimize formatting input

## 6. Final LLM Formatting

The final LLM chain generates a polished and professional response using the aggregated outputs.

### Purpose

- improve readability
- generate structured responses
- prepare email-ready content

### Responsibilities

- process merged AI outputs
- improve formatting quality
- create final response structure

## 7. Email Response

The processed AI response is automatically sent back to the user through Gmail.

### Purpose

- automated communication
- response delivery
- end-to-end workflow completion

### Responsibilities

- create outgoing email
- send AI-generated response
- complete workflow execution
