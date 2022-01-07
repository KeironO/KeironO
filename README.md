```python
from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Me:
    pronouns : tuple[str, ...] = ("He", "Him")
    org      : str             = "Cwm Taf University Health Board"
    role     : str             = "Advanced Information Analyst"
    languages: tuple[str, ...] = ("Python", "R", "Java")
    databases: tuple[str, ...] = ("MariaDB", "PostgreSQL", "Redis")
    
    misc     : tuple[str, ...] = ("Docker", "Flask", "Machine Learning", "Statistics")
    ongoing  : tuple[str, ...] = ("Ansible", "Julia", "Rust")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)        
```
