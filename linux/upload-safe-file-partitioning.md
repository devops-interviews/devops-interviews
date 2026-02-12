# Upload Safe File Partitioning

> **Company:** GoDaddy | **Difficulty:** Medium

---

#### **Scenario**

Your application uploads files from `/tmp/app/`, but the maximum allowed file size is 1 MB, and some files exceed this limit.

#### **Task**

Find all files larger than 1 MB in `/tmp/app/` and its subdirectories, split each oversized file into 1 MB chunks in the same directory where the original file is located with a recognizable naming pattern (e.g., original_filename.part_aa), keep the original files intact, and verify that the chunks were created successfully.

#### **Example**

```
# Before (files exceed 1 MB limit)

/tmp/app/uploads/video.mp4 (3.2 MB)
/tmp/app/data/archive.tar.gz (2.5 MB)

Cannot upload due to size restrictions
```

```
# After (files split into 1 MB chunks)

/tmp/app/uploads/video.mp4
/tmp/app/uploads/video.mp4.part_aa
/tmp/app/uploads/video.mp4.part_ab
/tmp/app/uploads/video.mp4.part_ac

/tmp/app/data/archive.tar.gz
/tmp/app/data/archive.tar.gz.part_aa
/tmp/app/data/archive.tar.gz.part_ab

Chunks ready for upload within size limits
```

---
📹 [Video Solution](https://prepare.sh/interview/devops/terminal/upload-safe-file-partitioning)
