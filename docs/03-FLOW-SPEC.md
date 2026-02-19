# FLOW SPEC

## 기본 패턴

Source → Transit → Process → Sink

---

## Node Types

1. SourceNode
2. TransitNode
3. ProcessNode
4. BufferNode
5. SinkNode

---

## Sink Types

- SINK_OUTBOUND
- SINK_STORAGE
- SINK_SORTER_INFEED
- SINK_REJECT

---

## Link Types

- ConveyorLink
- LiftLink
- VirtualLink