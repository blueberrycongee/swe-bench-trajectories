# SWE-bench Code Search Trajectories

Real code search trajectories for [SWE-bench Lite](https://github.com/princeton-nlp/SWE-bench) dataset.

## Dataset

**File:** `lite_all_expanded.json`

| Field | Description |
|-------|-------------|
| `instance_id` | Unique issue identifier |
| `repo` | GitHub repository name |
| `base_commit` | Base commit hash |
| `query` | Issue description |
| `patch` | Ground truth fix |
| `ground_truth.trajectory` | Search trajectory (grep/find/read calls) |
| `ground_truth.answer` | Target file(s) and line numbers |

## Statistics

- **Total issues:** 300
- **Source:** SWE-bench Lite

## Tool Call Format

```json
{"name": "grep", "arguments": {"pattern": "...", "path": "..."}}
{"name": "find", "arguments": {"pattern": "..."}}
{"name": "read", "arguments": {"file": "...", "start": N, "end": M}}
```

## Citation

If you use this dataset, please cite the original SWE-bench paper:

```bibtex
@inproceedings{jimenez2024swebench,
  title={SWE-bench: Can Language Models Resolve Real-world Github Issues?},
  author={Jimenez, Carlos E and Yang, John and Wettig, Alexander and Yao, Shunyu and Pei, Kexin and Press, Ofir and Narasimhan, Karthik},
  booktitle={ICLR},
  year={2024}
}
```

## License

MIT
