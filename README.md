# Galaxy python plugin API

## Usage

Implement plugin:

```python
import asyncio
from galaxy.api.plugin import Plugin

class PluginExample(Plugin):
    # implement methods
    async def authenticate(self, stored_credentials=None):
        pass

# run plugin event loop
if __name__ == "__main__":
    asyncio.run(MockPlugin().run())
```

Use [pyinstaller](https://www.pyinstaller.org/) to create plugin executbale.

## Development

Install required packages:
```bash
pip install -r requirements.txt
```

Run tests:
```bash
pytest
```