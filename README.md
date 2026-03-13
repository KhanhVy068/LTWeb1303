Báo cáo lập trình web nhóm 13
Các lỗi tìm được
File: orders.php       
Trước khi sửa:
foreach ($orders as $order) {
    if ($order['status'] === 'completed') {
        $pendingOnly[] = $order;
    }
}
Sau khi sửa: 
foreach ($orders as $order) {
    if ($order['status'] === 'pending') {
        $pendingOnly[] = $order;
    }
}


