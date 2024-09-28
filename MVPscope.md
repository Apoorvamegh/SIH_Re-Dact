# RE-DACT Proof-of-Concept: MVP Scope

## 1. Core Redaction Functionality

### Text Redaction
- **Named Entity Recognition (NER):** Implement basic NER to identify common sensitive information types:
  - Personal names
  - Locations (cities, countries)
  - Organizations
  - Dates
  - Phone numbers
  - Email addresses
- **Redaction Methods:**
  - Full masking (e.g., replacing with 'XXXX')
  - Partial masking (e.g., 'J*** D**')
  - Character substitution (e.g., replacing with random characters)

### Image Redaction
- **Face Detection:** Implement basic face detection in images
- **Text in Images:** Detect and redact visible text in images
- **Redaction Methods:**
  - Blurring (Gaussian blur)
  - Black box overlay

## 2. Input/Output Handling

### Supported Input Formats
- Plain text files (.txt)
- Common image formats (.jpg, .png)

### Output Generation
- Redacted text files
- Redacted images
- Simple log of redactions made

## 3. User Interface

### File Handling
- File upload mechanism for text and images
- Display of original and redacted content
- Download option for redacted files

### Redaction Controls
- Slider or dropdown for redaction intensity (Low, Medium, High)
- Checkboxes to select types of information to redact (e.g., names, dates, locations)

### Basic Visualization
- Side-by-side view of original and redacted content
- Highlight or marking of redacted areas in text

## 4. Processing Pipeline

- Basic preprocessing of text (tokenization, sentence splitting)
- Sequential application of selected redaction methods
- Simple error handling for unsupported file types or processing failures

## 5. Performance Considerations

- Ability to process files up to 5MB in size
- Response time under 30 seconds for text files up to 1000 words
- Handling of up to 5 concurrent users

## 6. Basic Security Measures

- Client-side file processing (no server-side storage of uploaded files)
- HTTPS implementation for the web interface
- Basic input sanitization to prevent common web vulnerabilities

## 7. Minimal Customization

- Option to add custom words or phrases to be redacted
- Basic regex support for custom redaction patterns

## 8. Simple Reporting

- Count of redactions made by type (e.g., 5 names, 3 dates redacted)
- Estimation of document sensitivity based on the number and type of redactions

## Out of Scope for MVP

- PDF or video file support
- Advanced NLP techniques (e.g., context-aware redaction)
- Synthetic data generation
- User authentication and multi-user support
- Undo/redo functionality
- Batch processing of multiple files

## Future Expansion Possibilities

- Integration with cloud storage services
- API for programmatic access
- Machine learning model for improved entity recognition
- Support for additional languages
- Advanced image redaction (object removal, inpainting)

