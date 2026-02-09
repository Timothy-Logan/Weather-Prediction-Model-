# Contributing to Weather Prediction Model

Thank you for your interest in contributing to the Weather Prediction Model! We welcome contributions from the community.

## Ways to Contribute

### 🐛 Report Bugs

Found a bug? Please open an issue with:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Your environment (OS, Python version, Docker version)
- Error messages or logs

### 💡 Suggest Features

Have an idea? Open an issue describing:
- The feature you'd like to see
- Why it would be useful
- Possible implementation approach
- Any relevant examples or references

### 📝 Improve Documentation

Documentation improvements are always welcome:
- Fix typos or unclear explanations
- Add examples or use cases
- Improve installation instructions
- Add troubleshooting tips

### 🔧 Submit Code

1. **Fork** the repository
2. **Create a branch** for your feature
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
   - Follow PEP 8 style guidelines
   - Add comments for complex logic
   - Update documentation if needed
   - Add docstrings to new functions
4. **Test your changes**
   - Ensure the API still works
   - Test Docker deployment
   - Verify all endpoints function correctly
5. **Commit with clear message**
   ```bash
   git commit -m "Add: temperature prediction for multiple locations"
   ```
6. **Push to your fork**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**
   - Describe your changes clearly
   - Reference any related issues
   - Include before/after examples if applicable

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/Weather-Prediction-Model-
cd Weather-Prediction-Model-

# Install dependencies
pip install -r requirements.txt

# Run the API locally
uvicorn main:app --reload

# Test endpoints
curl http://localhost:8000/
```

## Code Style Guidelines

- Follow [PEP 8](https://pep8.org/) Python style guide
- Use descriptive variable names (e.g., `temperature_data` not `td`)
- Add docstrings to all functions and classes
- Keep functions focused and under 50 lines when possible
- Comment complex logic and algorithms
- Use type hints for function parameters and returns

Example:
```python
def predict_temperature(data: list, days: int = 3) -> dict:
    """
    Predict future temperatures based on historical data.
    
    Args:
        data: List of historical temperature values
        days: Number of days to forecast (default: 3)
        
    Returns:
        Dictionary containing forecast and metadata
    """
    # Implementation here
```

## Testing

Before submitting a pull request:

1. **Test the API**:
   ```bash
   # Start the server
   uvicorn main:app --reload
   
   # Test in another terminal
   curl http://localhost:8000/
   curl -X POST http://localhost:8000/forecast -d '{"location": "Ajax", "data": [15, 16, 17]}'
   ```

2. **Test Docker deployment**:
   ```bash
   docker build -t weather-prediction .
   docker run -p 8000:8000 weather-prediction
   ```

3. **Check code style**:
   ```bash
   # Install flake8 if needed
   pip install flake8
   
   # Run linter
   flake8 *.py --max-line-length=100
   ```

## Project Structure

```
Weather-Prediction-Model-/
├── main.py              # FastAPI application
├── train_model.py       # Model training script
├── requirements.txt     # Python dependencies
├── Dockerfile          # Container configuration
├── README.md           # Project documentation
└── data_value.csv      # Sample data
```

## Adding New Features

### Want to add a new API endpoint?

1. Add the endpoint in `main.py`
2. Follow existing endpoint patterns
3. Add documentation in docstring
4. Update README with new endpoint details

### Want to improve the model?

1. Modify `train_model.py`
2. Document model changes
3. Include accuracy metrics
4. Update README with new performance stats

## Pull Request Process

1. Update the README.md with details of changes if applicable
2. Update requirements.txt if you add new dependencies
3. Your PR will be reviewed within 2-3 days
4. Address any feedback from reviewers
5. Once approved, your changes will be merged!

## Questions or Need Help?

Feel free to:
- Open an issue for discussion
- Email: [tjlogan9@gmail.com](mailto:tjlogan9@gmail.com)
- Check existing issues for similar questions

## Code of Conduct

### Our Standards

- Be respectful and constructive
- Welcome newcomers and help them learn
- Focus on what is best for the project
- Show empathy towards other contributors
- Give and accept constructive feedback gracefully

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or insulting comments
- Publishing others' private information
- Other conduct which could reasonably be considered inappropriate

## Recognition

Contributors will be:
- Listed in the project's acknowledgments
- Credited in release notes for their contributions
- Invited to collaborate on future enhancements

## License

By contributing, you agree that your contributions will be licensed under the project's MIT License.

---

Thank you for helping improve the Weather Prediction Model! 🌤️
