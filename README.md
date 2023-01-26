# voicevox-client
Unoffical API wrapper that you can use voicevox easy!

## Install
```sh
pip install voicevox-client
```

All that!

## Example
```python
from voicevox import Client
import asyncio


async def main():
    async with Client() as client:
        audio_query = await client.create_audio_query(
            "こんにちは！", speaker=1
        )
        with open("voice.wav", "wb") as f:
            f.write(await audio_query.synthesis())


if __name__ == "__main__":
    asyncio.run(main())
```
