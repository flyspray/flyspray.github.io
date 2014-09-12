---
layout: manual
title: Attachments
manual: tasks
order: 70
---

Files can be attached to [comments](/manual/comments) and tasks. The maximum file size depends on the server config (that is *min*(*memory_limit*, *post_max_size*, *upload_max_filesize*) and *file_uploads* must be enabled). If file uploads are not possible because of the server config, you will not (even if you are admin) have the permission to add attachments.

The attachments directory should be in the root of the install, and must contain an index.html file in order for attachements to work.

### Mime Types 

If you don't want to rely on auto-detection of file types, you can add options to `flyspray.conf.php`. Example:

<code>
[attachments]
zip="application/zip" ; ZIP = extension, application/zip = MIME-Type
</code>
