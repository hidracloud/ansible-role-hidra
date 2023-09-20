Hidra Exporter Ansible Role
===========================

**Hidra** is your online sentinel, monitoring your digital services and alerting you of any issues in real-time. With Hidra, you can rest assured that your online presence is constantly being watched and that any potential downtime is quickly identified and resolved. Keep your online business running smoothly with Hidra.

This Ansible role deploys and configures the Hidra Exporter, allowing you to easily integrate Hidra into your infrastructure for URL monitoring.

Default Variables
-----------------

Below are the default variables used by this Ansible role. You can override them as needed.

### System Configuration

*   **System Group:** `_hidra_exporter_system_group`: `hidra`
*   **System User:** `_hidra_exporter_system_user`: `hidra`
*   **Binary Installation Directory:** `_hidra_exporter_binary_install_dir`: `/usr/local/bin`
*   **Local Binary Directory:** `hidra_exporter_binary_local_dir`: `""`
*   **Version:** `hidra_exporter_version`: `3.2.0`
*   **Go Architecture:** `go_arch`: `amd64`

### Hidra Exporter Configuration

*   **Log Level:** `hidra_log_level`: `info`
*   **HTTP Listen Address:** `hidra_http_listen_address`: `:19090`
*   **Samples Path:** `hidra_samples_path`: `/etc/hidra_exporter/samples`
*   **Refresh Samples Interval:** `hidra_refresh_samples_interval`: `60s`
*   **Enqueue Samples Interval:** `hidra_enqueue_samples_interval`: `5s`
*   **Garbage Collection Interval:** `hidra_gc_interval`: `5m`
*   **Basic Auth:** `hidra_basic_auth_enabled`: `false`
    *   **Username:** `hidra_basic_auth_username`: `prometheus`
    *   **Password:** `hidra_basic_auth_password`: `prometheus`
*   **Worker:**
    *   **Parallel Jobs:** `hidra_worker_parallel_jobs`: `16`
    *   **Max Queue Size:** `hidra_max_queue_size`: `1000`
    *   **Sleep Between Jobs:** `hidra_sleep_between_jobs`: `1s`
*   **Reports:**
    *   **Enabled:** `hidra_report_enabled`: `false`
    *   **S3 Configuration:**
        *   **Enabled:** `hidra_s3_enabled`: `false`
        *   **Bucket:** `hidra_s3_bucket`: `hidra-reports`
        *   **Region:** `hidra_s3_region`: `""`
        *   **Access Key ID:** `hidra_s3_access_key_id`: `hidratest`
        *   **Secret Access Key:** `hidra_s3_secret_access_key`: `hidratest`
        *   **Endpoint:** `hidra_s3_endpoint`: `minio:9000`
        *   **Use SSL:** `hidra_s3_use_ssl`: `false`
    *   **Callback:**
        *   **Enabled:** `hidra_callback_enabled`: `false`
        *   **URL:** `hidra_callback_url`: `http://localhost:19091`
*   **Usage Collector:** `hidra_usage_enabled`: `true`

Installation
------------

1.  ...


Contributing
------------

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

License
-------

[GPL3](https://choosealicense.com/licenses/gpl-3.0/)