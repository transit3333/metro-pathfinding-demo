# Metro Pathfinding Demo

Demo web tìm đường trên mạng rail Chicago, so sánh BFS, DFS, Dijkstra, A* Lp và Greedy Best-First.

## Chạy demo web

Nên chạy bằng static server để trình duyệt đọc được file JSON:

```bash
python -m http.server 8000
```

Sau đó mở:

```text
http://localhost:8000/app.html
```

Các bước demo:

1. Bấm `Chicago` để đưa bản đồ về trung tâm.
2. Chọn `Pick Start`, click một điểm trên bản đồ.
3. Chọn `Pick End`, click điểm đích.
4. Bấm `Find Nearest Station Path` để xem route và bảng so sánh thuật toán.
5. Dùng `Mark Unusable` rồi click một đoạn ray để giả lập sự cố tuyến.

## Chạy benchmark

```bash
node data/algorithm_benchmark.js
```

## Cấu trúc chính

- `app.html`: giao diện demo.
- `style.css`: style cho demo.
- `data/mapapp.js`: điều khiển bản đồ, chọn điểm, render route, admin edge tools.
- `data/pathfinding.js`: dựng graph và chạy BFS/DFS/Dijkstra/A*/Greedy.
- `data/cta_rail_fallback.json`: dữ liệu rail network.
- `data/algorithm_benchmark.js`: benchmark thuật toán bằng Node.js.
