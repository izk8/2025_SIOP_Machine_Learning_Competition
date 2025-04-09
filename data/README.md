# Competition Dataset

This directory contains the datasets for the 2025 SIOP Machine Learning Competition.

## Dataset Structure

### Development Dataset (dev_dataset.zip)
The development dataset includes:
- `jobs.csv`: A spreadsheet with hiring jobs and their job descriptions
- `questions.csv`: A spreadsheet with jobs and the candidate questions

### Test Dataset (test_dataset.zip)
The test dataset will be made available on March 9, 2025 and will follow the same structure as the development dataset but with different jobs.

## Data Fields

### jobs.csv
- `job_id`: Unique identifier for each job
- `job_title`: Title of the job position
- `job_description`: Detailed description of the job
- `required_skills`: Skills required for the job
- `industry`: Industry sector of the job
- `company_size`: Size of the company offering the job

### questions.csv
- `job_id`: Unique identifier for each job (matches with jobs.csv)
- `question_id`: Unique identifier for each question
- `question_type`: Type of question (personality, cognitive ability, skills)
- `question_text`: The actual question text
- `response_type`: Format of expected response (multiple choice, text, etc.)
- `options`: Available options for multiple choice questions (JSON format)

## Scoring Components

The assessment includes three main components:

1. **Personality Assessment**
   - Based on IPIP-120
   - Includes GenAI generated Ipsative Questions
   - Personality-specific interview questions

2. **Cognitive Ability Assessment**
   - Numeric Patterns
   - Applying mathematical operations
   - Unscrambling/Anagrams

3. **Skills and Ability Assessment**
   - Interview questions scored with pretrained BARS cross-encoder
   - Technology knowledge assessment

4. **Honesty Score**
   - Composite of overclaiming and response patterns
   - Accuracy of detecting job-related technologies versus AI generated technologies
   - Pretrained model based on Nie et al., 2025 