<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blogging Platform - Complete Documentation with Screenshots</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica', 'Arial', sans-serif;
            line-height: 1.6;
            color: #24292e;
            background: #f6f8fa;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 60px;
        }

        .header h1 {
            font-size: 48px;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .badges {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .badge {
            display: inline-block;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 12px;
            font-weight: 600;
            text-decoration: none;
        }

        /* README Content Styles */
        .readme-section {
            background: white;
            padding: 40px;
            border-radius: 12px;
            margin-bottom: 30px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }

        .readme-section h2 {
            font-size: 32px;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #e1e4e8;
        }

        .readme-section h3 {
            font-size: 24px;
            margin: 30px 0 15px 0;
            color: #0366d6;
        }

        .readme-section h4 {
            font-size: 18px;
            margin: 20px 0 10px 0;
        }

        .readme-section p {
            margin-bottom: 15px;
            line-height: 1.8;
        }

        .readme-section ul, .readme-section ol {
            margin: 15px 0 15px 30px;
        }

        .readme-section li {
            margin-bottom: 8px;
        }

        code {
            background: #f6f8fa;
            padding: 3px 6px;
            border-radius: 3px;
            font-family: 'Courier New', monospace;
            font-size: 14px;
        }

        pre {
            background: #282c34;
            color: #abb2bf;
            padding: 20px;
            border-radius: 8px;
            overflow-x: auto;
            margin: 20px 0;
            font-size: 14px;
            line-height: 1.6;
        }

        pre code {
            background: none;
            color: inherit;
            padding: 0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        table th {
            background: #f6f8fa;
            padding: 12px;
            text-align: left;
            font-weight: 600;
            border: 1px solid #e1e4e8;
        }

        table td {
            padding: 12px;
            border: 1px solid #e1e4e8;
        }

        /* Screenshot Styles */
        .screenshot-wrapper {
            margin: 40px 0;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .screenshot-title {
            font-size: 24px;
            font-weight: 600;
            margin-bottom: 20px;
            color: #0366d6;
        }

        .screenshot-card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            margin-bottom: 40px;
            overflow: hidden;
        }

        .browser-bar {
            background: #e8eaed;
            padding: 12px 20px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .browser-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .dot-red { background: #ff5f56; }
        .dot-yellow { background: #ffbd2e; }
        .dot-green { background: #27c93f; }

        .url-bar {
            background: white;
            border-radius: 6px;
            padding: 6px 16px;
            margin-left: 12px;
            flex: 1;
            color: #5f6368;
            font-size: 13px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .screenshot-content {
            background: #f5f7fa;
        }

        /* Dashboard Styles */
        .dashboard {
            padding: 30px;
            min-height: 600px;
        }

        .dashboard-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 30px;
        }

        .dashboard-header h1 {
            font-size: 32px;
            margin-bottom: 8px;
        }

        .dashboard-header p {
            opacity: 0.9;
            font-size: 16px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            border-left: 4px solid;
        }

        .stat-card.posts { border-left-color: #667eea; }
        .stat-card.users { border-left-color: #f093fb; }
        .stat-card.categories { border-left-color: #4facfe; }
        .stat-card.views { border-left-color: #43e97b; }

        .stat-card h3 {
            color: #666;
            font-size: 14px;
            text-transform: uppercase;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .stat-number {
            font-size: 36px;
            font-weight: bold;
            color: #333;
            margin-bottom: 8px;
        }

        .stat-change {
            font-size: 13px;
            color: #43e97b;
        }

        .recent-posts {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .recent-posts h2 {
            margin-bottom: 20px;
            color: #333;
            font-size: 20px;
            border: none;
            padding: 0;
        }

        .post-item {
            padding: 15px;
            border-bottom: 1px solid #e8eaed;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .post-item:last-child {
            border-bottom: none;
        }

        .post-info h4 {
            color: #333;
            margin-bottom: 5px;
            font-size: 15px;
        }

        .post-meta {
            font-size: 13px;
            color: #666;
        }

        .status-badge {
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }

        .status-published {
            background: #d4edda;
            color: #155724;
        }

        .status-draft {
            background: #fff3cd;
            color: #856404;
        }

        /* Post List Styles */
        .post-list {
            padding: 30px;
            min-height: 600px;
        }

        .page-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }

        .page-header h1 {
            font-size: 28px;
            color: #333;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.4);
        }

        .filters {
            background: white;
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 20px;
            display: flex;
            gap: 15px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .filter-input {
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            flex: 1;
        }

        .table-container {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .data-table {
            width: 100%;
            border-collapse: collapse;
        }

        .data-table thead {
            background: #f8f9fa;
        }

        .data-table th {
            padding: 15px;
            text-align: left;
            font-weight: 600;
            color: #333;
            font-size: 13px;
            text-transform: uppercase;
            border-bottom: 2px solid #e8eaed;
        }

        .data-table td {
            padding: 15px;
            border-bottom: 1px solid #f0f0f0;
            color: #666;
            font-size: 14px;
        }

        .data-table tbody tr:hover {
            background: #f8f9fa;
        }

        .action-buttons {
            display: flex;
            gap: 8px;
        }

        .btn-edit, .btn-delete, .btn-view {
            padding: 6px 12px;
            border-radius: 6px;
            font-size: 12px;
            border: none;
            cursor: pointer;
            font-weight: 600;
        }

        .btn-edit {
            background: #e3f2fd;
            color: #1976d2;
        }

        .btn-delete {
            background: #ffebee;
            color: #c62828;
        }

        .btn-view {
            background: #e8f5e9;
            color: #2e7d32;
        }

        /* Post Editor Styles */
        .post-editor {
            padding: 30px;
            min-height: 700px;
        }

        .editor-container {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #333;
            font-size: 14px;
        }

        .form-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            font-family: inherit;
        }

        textarea.form-input {
            min-height: 200px;
            resize: vertical;
        }

        .editor-toolbar {
            background: #f8f9fa;
            padding: 10px;
            border-radius: 8px 8px 0 0;
            border: 1px solid #ddd;
            border-bottom: none;
            display: flex;
            gap: 8px;
        }

        .toolbar-btn {
            padding: 8px 12px;
            background: white;
            border: 1px solid #ddd;
            border-radius: 6px;
            cursor: pointer;
            font-size: 13px;
            color: #666;
        }

        .rich-editor {
            border: 1px solid #ddd;
            border-radius: 0 0 8px 8px;
            padding: 15px;
            min-height: 250px;
            background: white;
            font-size: 14px;
            line-height: 1.6;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .editor-actions {
            display: flex;
            gap: 15px;
            justify-content: flex-end;
            margin-top: 30px;
        }

        .btn-secondary {
            background: #e8eaed;
            color: #333;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
        }

        /* User Management Styles */
        .user-management {
            padding: 30px;
            min-height: 600px;
        }

        .user-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 15px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .user-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            font-weight: bold;
        }

        .user-details {
            flex: 1;
        }

        .user-details h3 {
            margin-bottom: 5px;
            color: #333;
        }

        .user-details p {
            color: #666;
            font-size: 14px;
            margin: 0;
        }

        .role-badge {
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            text-transform: uppercase;
        }

        .role-admin {
            background: #ffebee;
            color: #c62828;
        }

        .role-editor {
            background: #e3f2fd;
            color: #1976d2;
        }

        .role-reader {
            background: #e8f5e9;
            color: #2e7d32;
        }

        /* API Response Styles */
        .api-response {
            padding: 30px;
            min-height: 600px;
        }

        .postman-interface {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .postman-header {
            background: #ff6c37;
            padding: 15px 20px;
            color: white;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .postman-logo {
            font-size: 20px;
            font-weight: bold;
        }

        .request-bar {
            background: #f8f9fa;
            padding: 20px;
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .method-select {
            padding: 10px 15px;
            background: #43e97b;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 13px;
        }

        .url-input {
            flex: 1;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 14px;
        }

        .send-btn {
            padding: 10px 30px;
            background: #ff6c37;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
        }

        .response-section {
            padding: 20px;
        }

        .response-tabs {
            display: flex;
            gap: 20px;
            margin-bottom: 15px;
            border-bottom: 2px solid #e8eaed;
        }

        .tab {
            padding: 10px 0;
            color: #666;
            cursor: pointer;
            position: relative;
        }

        .tab.active {
            color: #ff6c37;
            font-weight: 600;
        }

        .tab.active::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            right: 0;
            height: 2px;
            background: #ff6c37;
        }

        .response-info {
            display: flex;
            gap: 20px;
            margin-bottom: 15px;
            font-size: 13px;
        }

        .response-info span {
            color: #666;
        }

        .response-info .success {
            color: #43e97b;
            font-weight: 600;
        }

        .json-viewer {
            background: #282c34;
            color: #abb2bf;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 13px;
            line-height: 1.6;
            overflow-x: auto;
            max-height: 400px;
            overflow-y: auto;
        }

        .json-key {
            color: #e06c75;
        }

        .json-string {
            color: #98c379;
        }

        .json-number {
            color: #d19a66;
        }

        .json-boolean {
            color: #56b6c2;
        }

        .screenshot-description {
            margin-top: 20px;
            padding: 15px;
            background: #f6f8fa;
            border-left: 4px solid #0366d6;
            border-radius: 4px;
        }

        .screenshot-description h4 {
            color: #0366d6;
            margin-bottom: 10px;
        }

        .screenshot-description ul {
            margin-left: 20px;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .feature-card {
            background: #f6f8fa;
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid #0366d6;
        }

        .feature-card h4 {
            color: #0366d6;
            margin-bottom: 10px;
        }

        .feature-card ul {
            list-style: none;
            padding: 0;
        }

        .feature-card li:before {
            content: "✓ ";
            color: #28a745;
            font-weight: bold;
            margin-right: 8px;
        }

        .copy-button {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 8px 24px rgba(102, 126, 234, 0.4);
            z-index: 1000;
        }

        .copy-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 32px rgba(102, 126, 234, 0.5);
        }

        @media print {
            .copy-button {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>✨ Cloud-Hosted Blogging Platform</h1>
            <p style="font-size: 18px; color: #666; margin-bottom: 20px;">Django-Based Backend System with Role-Based Access Control</p>
            
            <div class="badges">
                <span class="badge" style="background: #3776AB; color: white;">Python 3.9+</span>
                <span class="badge" style="background: #092E20; color: white;">Django 4.2</span>
                <span class="badge" style="background: #4479A1; color: white;">MySQL 8.0</span>
                <span class="badge" style="background: #009688; color: white;">REST API</span>
                <span class="badge" style="background: #0089D6; color: white;">Cloud Deployed</span>
            </div>

            <p style="font-size: 16px; margin-top: 20px;">
                <strong>A production-ready blogging platform with enterprise-grade security, role-based access control, and RESTful API architecture.</strong>
            </p>
        </div>

        <!-- Overview Section -->
        <div class="readme-section">
            <h2>🎯 Overview</h2>
            <p>The <strong>Cloud-Hosted Blogging Platform</strong> is a Django-based backend system designed to provide a secure, scalable solution for content management. Built with modern web development best practices, this platform demonstrates enterprise-level architecture with role-based access control (RBAC), RESTful API design, and cloud deployment capabilities.</p>
            
            <h3>🎯 Project Goals</h3>
            <ul>
                <li>✅ Implement secure authentication and authorization</li>
                <li>✅ Design scalable RESTful APIs</li>
                <li>✅ Optimize database queries for performance</li>
                <li>✅ Deploy on cloud infrastructure</li>
                <li>✅ Follow clean code principles and best practices</li>
            </ul>

            <h3>📅 Development Timeline</h3>
            <p><strong>Duration:</strong> March 2025 - May 2025 (3 months)</p>
        </div>

        <!-- Features Section -->
        <div class="readme-section">
            <h2>✨ Features</h2>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <h4>🔐 Security & Authentication</h4>
                    <ul>
                        <li>JWT-based authentication</li>
                        <li>Secure password hashing (bcrypt)</li>
                        <li>CSRF protection</li>
                        <li>Role-based access control (RBAC)</li>
                        <li>Session management</li>
                        <li>Rate limiting for API endpoints</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>📝 Blog Management</h4>
                    <ul>
                        <li>Create, Read, Update, Delete (CRUD) operations</li>
                        <li>Draft and publish workflows</li>
                        <li>Rich text editor support</li>
                        <li>Image upload functionality</li>
                        <li>Tag and category management</li>
                        <li>Search and filter capabilities</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>👥 User Roles</h4>
                    <ul>
                        <li><strong>Admin:</strong> Full system access</li>
                        <li><strong>Editor:</strong> Create and edit content</li>
                        <li><strong>Reader:</strong> View published content</li>
                        <li>Custom permission groups</li>
                        <li>Role assignment and management</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>🚀 Performance</h4>
                    <ul>
                        <li>Optimized MySQL queries</li>
                        <li>Database indexing</li>
                        <li>Query caching</li>
                        <li>Pagination for large datasets</li>
                        <li>Lazy loading</li>
                        <li>API response optimization</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Tech Stack Section -->
        <div class="readme-section">
            <h2>🛠️ Tech Stack</h2>
            
            <h3>Backend Framework</h3>
            <p>
                <span class="badge" style="background: #3776AB; color: white;">Python</span>
                <span class="badge" style="background: #092E20; color: white;">Django</span>
                <span class="badge" style="background: #ff1709; color: white;">Django REST Framework</span>
            </p>

            <h3>Database</h3>
            <p><span class="badge" style="background: #4479A1; color: white;">MySQL</span></p>

            <h3>Authentication & Security</h3>
            <p>
                <span class="badge" style="background: #000000; color: white;">JWT</span>
                <span class="badge" style="background: #4285F4; color: white;">OAuth 2.0</span>
            </p>

            <h3>Cloud & Deployment</h3>
            <p>
                <span class="badge" style="background: #0078D4; color: white;">Microsoft Azure</span>
                <span class="badge" style="background: #2CA5E0; color: white;">Docker</span>
                <span class="badge" style="background: #009639; color: white;">Nginx</span>
            </p>

            <h3>Development Tools</h3>
            <p>
                <span class="badge" style="background: #F05032; color: white;">Git</span>
                <span class="badge" style="background: #181717; color: white;">GitHub</span>
                <span class="badge" style="background: #007ACC; color: white;">VS Code</span>
                <span class="badge" style="background: #FF6C37; color: white;">Postman</span>
            </p>
        </div>

        <!-- Screenshots Section -->
        <div class="readme-section">
            <h2>📸 Screenshots</h2>
            <p>Below are the professional mockups showcasing the key features of the blogging platform:</p>
        </div>

        <!-- Screenshot 1: Dashboard -->
        <div class="screenshot-wrapper">
            <h3 class="screenshot-title">1️⃣ Dashboard Overview</h3>
            
            <div class="screenshot-card">
                <div class="browser-bar">
                    <div class="browser-dot dot-red"></div>
                    <div class="browser-dot dot-yellow"></div>
                    <div class="browser-dot dot-green"></div>
                    <div class="url-bar">
                        <span>🔒</span>
                        <span>https://blogging-platform.azurewebsites.net/dashboard</span>
                    </div>
                </div>
                <div class="screenshot-content">
                    <div class="dashboard">
                        <div class="dashboard-header">
                            <h1>👋 Welcome back, Admin!</h1>
                            <p>Here's what's happening with your blog today</p>
                        </div>

                        <div class="stats-grid">
                            <div class="stat-card posts">
                                <h3>Total Posts</h3>
                                <div class="stat-number">156</div>
                                <div class="stat-change">↑ 12% from last month</div>
                            </div>
                            <div class="stat-card users">
                                <h3>Active Users</h3>
                                <div class="stat-number">48</div>
                                <div class="stat-change">↑ 8% from last month</div>
                            </div>
                            <div class="stat-card categories">
                                <h3>Categories</h3>
                                <div class="stat-number">12</div>
                                <div class="stat-change">→ No change</div>
                            </div>
                            <div class="stat-card views">
                                <h3>Total Views</h3>
                                <div class="stat-number">24.5K</div>
                                <div class="stat-change">↑ 23% from last month</div>
                            </div>
                        </div>

                        <div class="recent-posts">
                            <h2>📝 Recent Posts</h2>
                            <div class="post-item">
                                <div class="post-info">
                                    <h4>Getting Started with Django REST Framework</h4>
                                    <div class="post-meta">by John Doe • 2 hours ago</div>
                                </div>
                                <span class="status-badge status-published">Published</span>
                            </div>
                            <div class="post-item">
                                <div class="post-info">
                                    <h4>Advanced MySQL Query Optimization Techniques</h4>
                                    <div class="post-meta">by Sarah Smith • 5 hours ago</div>
                                </div>
                                <span class="status-badge status-published">Published</span>
                            </div>
                            <div class="post-item">
                                <div class="post-info">
                                    <h4>Building Scalable Backend Systems</h4>
                                    <div class="post-meta">by Mike Johnson • 1 day ago</div>
                                </div>
                                <span class="status-badge status-draft">Draft</span>
                            </div>
                            <div class="post-item">
                                <div class="post-info">
                                    <h4>Understanding Role-Based Access Control</h4>
                                    <div class="post-meta">by Emily Davis • 2 days ago</div>
                                </div>
                                <span class="status-badge status-published">Published</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="screenshot-description">
                <h4>Features Shown:</h4>
                <ul>
                    <li>Real-time statistics cards (Posts, Users, Categories, Views)</li>
                    <li>Growth metrics and trends</li>
                    <li>Recent posts activity feed</li>
                    <li>Professional gradient design</li>
                    <li>Status indicators for content</li>
                </ul>
            </div>
        </div>

        <!-- Screenshot 2: Post List -->
        <div class="screenshot-wrapper">
            <h3 class="screenshot-title">2️⃣ Blog Post Management</h3>
            
            <div class="screenshot-card">
                <div class="browser-bar">
                    <div class="browser-dot dot-red"></div>
                    <div class="browser-dot dot-yellow"></div>
                    <div class="browser-dot dot-green"></div>
                    <div class="url-bar">
                        <span>🔒</span>
                        <span>https://blogging-platform.azurewebsites.net/posts</span>
                    </div>
                </div>
                <div class="screenshot-content">
                    <div class="post-list">
                        <div class="page-header">
                            <h1>📚 All Blog Posts</h1>
                            <button class="btn-primary">+ New Post</button>
                        </div>

                        <div class="filters">
                            <input type="text" class="filter-input" placeholder="🔍 Search posts...">
                            <select class="filter-input" style="flex: 0.3;">
                                <option>All Status</option>
                                <option>Published</option>
                                <option>Draft</option>
                                <option>Archived</option>
                            </select>
                            <select class="filter-input" style="flex: 0.3;">
                                <option>All Categories</option>
                                <option>Web Development</option>
                                <option>Database</option>
                                <option>Cloud</option>
                            </select>
                        </div>

                        <div class="table-container">
                            <table class="data-table">
                                <thead>
                                    <tr>
                                        <th>TITLE</th>
                                        <th>AUTHOR</th>
                                        <th>CATEGORY</th>
                                        <th>STATUS</th>
                                        <th>CREATED</th>
                                        <th>ACTIONS</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td><strong>Django REST Framework Tutorial</strong></td>
                                        <td>John Doe</td>
                                        <td>Web Development</td>
                                        <td><span class="status-badge status-published">Published</span></td>
                                        <td>Mar 15, 2025</td>
                                        <td>
                                            <div class="action-buttons">
                                                <button class="btn-view">View</button>
                                                <button class="btn-edit">Edit</button>
                                                <button class="btn-delete">Delete</button>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td><strong>MySQL Optimization Guide</strong></td>
                                        <td>Sarah Smith</td>
                                        <td>Database</td>
                                        <td><span class="status-badge status-published">Published</span></td>
                                        <td>Mar 14, 2025</td>
                                        <td>
                                            <div class="action-buttons">
                                                <button class="btn-view">View</button>
                                                <button class="btn-edit">Edit</button>
                                                <button class="btn-delete">Delete</button>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td><strong>Building Scalable Systems</strong></td>
                                        <td>Mike Johnson</td>
                                        <td>Architecture</td>
                                        <td><span class="status-badge status-draft">Draft</span></td>
                                        <td>Mar 13, 2025</td>
                                        <td>
                                            <div class="action-buttons">
                                                <button class="btn-view">View</button>
                                                <button class="btn-edit">Edit</button>
                                                <button class="btn-delete">Delete</button>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td><strong>RBAC Implementation</strong></td>
                                        <td>Emily Davis</td>
                                        <td>Security</td>
                                        <td><span class="status-badge status-published">Published</span></td>
                                        <td>Mar 12, 2025</td>
                                        <td>
                                            <div class="action-buttons">
                                                <button class="btn-view">View</button>
                                                <button class="btn-edit">Edit</button>
                                                <button class="btn-delete">Delete</button>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td><strong>Cloud Deployment Best Practices</strong></td>
                                        <td>Alex Chen</td>
                                        <td>Cloud</td>
                                        <td><span class="status-badge status-published">Published</span></td>
                                        <td>Mar 11, 2025</td>
                                        <td>
                                            <div class="action-buttons">
                                                <button class="btn-view">View</button>
                                                <button class="btn-edit">Edit</button>
                                                <button class="btn-delete">Delete</button>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>

            <div class="screenshot-description">
                <h4>Features Shown:</h4>
                <ul>
                    <li>Advanced search and filter system</li>
                    <li>Sortable data table with pagination</li>
                    <li>Status badges (Published/Draft/Archived)</li>
                    <li>Bulk action capabilities</li>
                    <li>Quick action buttons (View/Edit/Delete)</li>
                    <li>Author and category information</li>
                </ul>
            </div>
        </div>

        <!-- Screenshot 3: Post Editor -->
        <div class="screenshot-wrapper">
            <h3 class="screenshot-title">3️⃣ Rich Text Post Editor</h3>
            
            <div class="screenshot-card">
                <div class="browser-bar">
                    <div class="browser-dot dot-red"></div>
                    <div class="browser-dot dot-yellow"></div>
                    <div class="browser-dot dot-green"></div>
                    <div class="url-bar">
                        <span>🔒</span>
                        <span>https://blogging-platform.azurewebsites.net/posts/create</span>
                    </div>
                </div>
                <div class="screenshot-content">
                    <div class="post-editor">
                        <div class="page-header">
                            <h1>✍️ Create New Post</h1>
                        </div>

                        <div class="editor-container">
                            <div class="form-group">
                                <label>Post Title *</label>
                                <input type="text" class="form-input" placeholder="Enter your post title..." value="Advanced Django Patterns for Production">
                            </div>

                            <div class="form-row">
                                <div class="form-group">
                                    <label>Category *</label>
                                    <select class="form-input">
                                        <option>Select category...</option>
                                        <option selected>Web Development</option>
                                        <option>Database</option>
                                        <option>Cloud</option>
                                        <option>Security</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label>Tags</label>
                                    <input type="text" class="form-input" placeholder="django, python, backend" value="django, python, rest-api">
                                </div>
                            </div>

                            <div class="form-group">
                                <label>Content *</label>
                                <div class="editor-toolbar">
                                    <button class="toolbar-btn"><strong>B</strong></button>
                                    <button class="toolbar-btn"><em>I</em></button>
                                    <button class="toolbar-btn"><u>U</u></button>
                                    <button class="toolbar-btn">H1</button>
                                    <button class="toolbar-btn">H2</button>
                                    <button class="toolbar-btn">• List</button>
                                    <button class="toolbar-btn">1. List</button>
                                    <button class="toolbar-btn">🔗 Link</button>
                                    <button class="toolbar-btn">📷 Image</button>
                                    <button class="toolbar-btn">💻 Code</button>
                                </div>
                                <div class="rich-editor">
                                    <p><strong>Introduction</strong></p>
                                    <p>Django is a powerful Python web framework that makes it easy to build robust web applications. In this comprehensive guide, we'll explore advanced patterns that will help you build production-ready applications.</p>
                                    <br>
                                    <p><strong>Key Topics Covered:</strong></p>
                                    <ul style="margin-left: 20px; margin-top: 10px;">
                                        <li>Advanced Django ORM techniques</li>
                                        <li>Custom middleware development</li>
                                        <li>Performance optimization strategies</li>
                                        <li>Caching implementation</li>
                                    </ul>
                                </div>
                            </div>

                            <div class="form-row">
                                <div class="form-group">
                                    <label>Featured Image</label>
                                    <input type="file" class="form-input">
                                </div>
                                <div class="form-group">
                                    <label>Status *</label>
                                    <select class="form-input">
                                        <option selected>Draft</option>
                                        <option>Published</option>
                                        <option>Archived</option>
                                    </select>
                                </div>
                            </div>

                            <div class="editor-actions">
                                <button class="btn-secondary">Cancel</button>
                                <button class="btn-secondary">Save Draft</button>
                                <button class="btn-primary">Publish Post</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="screenshot-description">
                <h4>Features Shown:</h4>
                <ul>
                    <li>Rich text editor with formatting toolbar</li>
                    <li>Category and tag multi-select</li>
                    <li>Image upload with preview</li>
                    <li>Draft/Publish workflow</li>
                    <li>Auto-save functionality</li>
                    <li>SEO-friendly slug generation</li>
                    <li>Real-time preview</li>
                </ul>
            </div>
        </div>

        <!-- Screenshot 4: User Management -->
        <div class="screenshot-wrapper">
            <h3 class="screenshot-title">4️⃣ User Management (RBAC)</h3>
            
            <div class="screenshot-card">
                <div class="browser-bar">
                    <div class="browser-dot dot-red"></div>
                    <div class="browser-dot dot-yellow"></div>
                    <div class="browser-dot dot-green"></div>
                    <div class="url-bar">
                        <span>🔒</span>
                        <span>https://blogging-platform.azurewebsites.net/users</span>
                    </div>
                </div>
                <div class="screenshot-content">
                    <div class="user-management">
                        <div class="page-header">
                            <h1>👥 User Management</h1>
                            <button class="btn-primary">+ Add User</button>
                        </div>

                        <div class="filters" style="margin-bottom: 30px;">
                            <input type="text" class="filter-input" placeholder="🔍 Search users...">
                            <select class="filter-input" style="flex: 0.3;">
                                <option>All Roles</option>
                                <option>Admin</option>
                                <option>Editor</option>
                                <option>Reader</option>
                            </select>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">AD</div>
                            <div class="user-details">
                                <h3>Admin User</h3>
                                <p>admin@blogging-platform.com • Joined Mar 1, 2025</p>
                            </div>
                            <span class="role-badge role-admin">Admin</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">JD</div>
                            <div class="user-details">
                                <h3>John Doe</h3>
                                <p>john.doe@example.com • Joined Mar 5, 2025</p>
                            </div>
                            <span class="role-badge role-editor">Editor</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">SS</div>
                            <div class="user-details">
                                <h3>Sarah Smith</h3>
                                <p>sarah.smith@example.com • Joined Mar 7, 2025</p>
                            </div>
                            <span class="role-badge role-editor">Editor</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">MJ</div>
                            <div class="user-details">
                                <h3>Mike Johnson</h3>
                                <p>mike.j@example.com • Joined Mar 10, 2025</p>
                            </div>
                            <span class="role-badge role-reader">Reader</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">ED</div>
                            <div class="user-details">
                                <h3>Emily Davis</h3>
                                <p>emily.davis@example.com • Joined Mar 12, 2025</p>
                            </div>
                            <span class="role-badge role-editor">Editor</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>

                        <div class="user-card">
                            <div class="user-avatar">AC</div>
                            <div class="user-details">
                                <h3>Alex Chen</h3>
                                <p>alex.chen@example.com • Joined Mar 14, 2025</p>
                            </div>
                            <span class="role-badge role-reader">Reader</span>
                            <div class="action-buttons">
                                <button class="btn-edit">Edit</button>
                                <button class="btn-delete">Remove</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="screenshot-description">
                <h4>Features Shown:</h4>
                <ul>
                    <li>User cards with avatar placeholders</li>
                    <li>Role-based badges (Admin/Editor/Reader)</li>
                    <li>User search and filtering</li>
                    <li>Quick role assignment</li>
                    <li>Account status indicators</li>
                    <li>Batch user operations</li>
                </ul>
            </div>
        </div>

        <!-- Screenshot 5: API Response -->
        <div class="screenshot-wrapper">
            <h3 class="screenshot-title">5️⃣ REST API Response (Postman)</h3>
            
            <div class="screenshot-card">
                <div class="browser-bar">
                    <div class="browser-dot dot-red"></div>
                    <div class="browser-dot dot-yellow"></div>
                    <div class="browser-dot dot-green"></div>
                    <div class="url-bar">
                        <span>🔒</span>
                        <span>Postman - API Testing</span>
                    </div>
                </div>
                <div class="screenshot-content">
                    <div class="api-response">
                        <div class="postman-interface">
                            <div class="postman-header">
                                <div class="postman-logo">⚡ Postman</div>
                            </div>

                            <div class="request-bar">
                                <select class="method-select">
                                    <option>GET</option>
                                </select>
                                <input type="text" class="url-input" value="https://blogging-platform.azurewebsites.net/api/v1/posts/" readonly>
                                <button class="send-btn">Send</button>
                            </div>

                            <div class="response-section">
                                <div class="response-tabs">
                                    <div class="tab active">Body</div>
                                    <div class="tab">Headers</div>
                                    <div class="tab">Test Results</div>
                                </div>

                                <div class="response-info">
                                    <span class="success">Status: 200 OK</span>
                                    <span>Time: 142 ms</span>
                                    <span>Size: 2.3 KB</span>
                                </div>

                                <div class="json-viewer">{
  <span class="json-key">"count"</span>: <span class="json-number">156</span>,
  <span class="json-key">"next"</span>: <span class="json-string">"https://blogging-platform.azurewebsites.net/api/v1/posts/?page=2"</span>,
  <span class="json-key">"previous"</span>: <span class="json-boolean">null</span>,
  <span class="json-key">"results"</span>: [
    {
      <span class="json-key">"id"</span>: <span class="json-number">1</span>,
      <span class="json-key">"title"</span>: <span class="json-string">"Getting Started with Django REST Framework"</span>,
      <span class="json-key">"slug"</span>: <span class="json-string">"getting-started-with-django-rest-framework"</span>,
      <span class="json-key">"content"</span>: <span class="json-string">"Django REST Framework is a powerful toolkit..."</span>,
      <span class="json-key">"author"</span>: {
        <span class="json-key">"id"</span>: <span class="json-number">1</span>,
        <span class="json-key">"username"</span>: <span class="json-string">"john_doe"</span>,
        <span class="json-key">"email"</span>: <span class="json-string">"john.doe@example.com"</span>
      },
      <span class="json-key">"status"</span>: <span class="json-string">"published"</span>,
      <span class="json-key">"featured_image"</span>: <span class="json-string">"/media/posts/django-rest.jpg"</span>,
      <span class="json-key">"categories"</span>: [
        {
          <span class="json-key">"id"</span>: <span class="json-number">1</span>,
          <span class="json-key">"name"</span>: <span class="json-string">"Web Development"</span>,
          <span class="json-key">"slug"</span>: <span class="json-string">"web-development"</span>
        }
      ],
      <span class="json-key">"tags"</span>: [
        {<span class="json-key">"id"</span>: <span class="json-number">1</span>, <span class="json-key">"name"</span>: <span class="json-string">"Django"</span>, <span class="json-key">"slug"</span>: <span class="json-string">"django"</span>},
        {<span class="json-key">"id"</span>: <span class="json-number">2</span>, <span class="json-key">"name"</span>: <span class="json-string">"Python"</span>, <span class="json-key">"slug"</span>: <span class="json-string">"python"</span>},
        {<span class="json-key">"id"</span>: <span class="json-number">3</span>, <span class="json-key">"name"</span>: <span class="json-string">"REST API"</span>, <span class="json-key">"slug"</span>: <span class="json-string">"rest-api"</span>}
      ],
      <span class="json-key">"created_at"</span>: <span class="json-string">"2025-03-15T10:30:00Z"</span>,
      <span class="json-key">"updated_at"</span>: <span class="json-string">"2025-03-16T14:20:00Z"</span>,
      <span class="json-key">"published_at"</span>: <span class="json-string">"2025-03-15T12:00:00Z"</span>
    }
  ]
}</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="screenshot-description">
                <h4>Features Shown:</h4>
                <ul>
                    <li>GET request to /api/v1/posts/ endpoint</li>
                    <li>JSON response with proper formatting</li>
                    <li>Status code: 200 OK</li>
                    <li>Response time metrics</li>
                    <li>Syntax-highlighted JSON</li>
                    <li>Complete data structure with nested objects</li>
                    <li>Pagination metadata</li>
                </ul>
            </div>
        </div>

        <!-- Installation Section -->
        <div class="readme-section">
            <h2>🚀 Installation</h2>

            <h3>Prerequisites</h3>
            <ul>
                <li>Python 3.9 or higher</li>
                <li>MySQL 8.0 or higher</li>
                <li>pip (Python package manager)</li>
                <li>Git</li>
            </ul>

            <h3>Step 1: Clone the Repository</h3>
            <pre><code>git clone https://github.com/NihaRuksar/blogging-platform.git
cd blogging-platform</code></pre>

            <h3>Step 2: Create Virtual Environment</h3>
            <pre><code># Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate</code></pre>

            <h3>Step 3: Install Dependencies</h3>
            <pre><code>pip install -r requirements.txt</code></pre>

            <h3>Step 4: Configure Database</h3>
            <p>Create a <code>.env</code> file in the project root:</p>
            <pre><code># Database Configuration
DB_NAME=blogging_platform
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_HOST=localhost
DB_PORT=3306

# Django Settings
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1

# JWT Settings
JWT_SECRET_KEY=your-jwt-secret-key
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30</code></pre>

            <h3>Step 5: Create MySQL Database</h3>
            <pre><code>mysql -u root -p</code></pre>
            <pre><code>CREATE DATABASE blogging_platform CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
EXIT;</code></pre>

            <h3>Step 6: Run Migrations</h3>
            <pre><code>python manage.py makemigrations
python manage.py migrate</code></pre>

            <h3>Step 7: Create Superuser</h3>
            <pre><code>python manage.py createsuperuser</code></pre>

            <h3>Step 8: Run Development Server</h3>
            <pre><code>python manage.py runserver</code></pre>

            <p>Visit <code>http://localhost:8000</code> to see the application running! 🎉</p>
        </div>

        <!-- API Documentation Section -->
        <div class="readme-section">
            <h2>📚 API Documentation</h2>

            <h3>Base URL</h3>
            <pre><code>http://localhost:8000/api/v1/</code></pre>

            <h3>Authentication</h3>
            <p>All protected endpoints require JWT token in the header:</p>
            <pre><code>Authorization: Bearer &lt;your_jwt_token&gt;</code></pre>

            <h3>Authentication Endpoints</h3>

            <h4>Register User</h4>
            <pre><code>POST /api/v1/auth/register/</code></pre>
            <p><strong>Request Body:</strong></p>
            <pre><code>{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "SecurePass123!",
  "role": "reader"
}</code></pre>

            <h4>Login</h4>
            <pre><code>POST /api/v1/auth/login/</code></pre>
            <p><strong>Request Body:</strong></p>
            <pre><code>{
  "username": "john_doe",
  "password": "SecurePass123!"
}</code></pre>

            <h3>Blog Post Endpoints</h3>

            <h4>Get All Posts</h4>
            <pre><code>GET /api/v1/posts/</code></pre>
            <p><strong>Query Parameters:</strong></p>
            <ul>
                <li><code>page</code> (int): Page number for pagination</li>
                <li><code>limit</code> (int): Items per page (default: 10)</li>
                <li><code>status</code> (string): Filter by status (draft, published, archived)</li>
                <li><code>author</code> (int): Filter by author ID</li>
                <li><code>search</code> (string): Search in title and content</li>
            </ul>

            <h4>Create Post (Editor/Admin only)</h4>
            <pre><code>POST /api/v1/posts/</code></pre>

            <h4>Update Post (Editor/Admin only)</h4>
            <pre><code>PUT /api/v1/posts/{id}/
PATCH /api/v1/posts/{id}/</code></pre>

            <h4>Delete Post (Admin only)</h4>
            <pre><code>DELETE /api/v1/posts/{id}/</code></pre>

            <h3>API Response Codes</h3>
            <table>
                <thead>
                    <tr>
                        <th>Status Code</th>
                        <th>Meaning</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>200</td>
                        <td>OK - Request successful</td>
                    </tr>
                    <tr>
                        <td>201</td>
                        <td>Created - Resource created successfully</td>
                    </tr>
                    <tr>
                        <td>204</td>
                        <td>No Content - Resource deleted successfully</td>
                    </tr>
                    <tr>
                        <td>400</td>
                        <td>Bad Request - Invalid input</td>
                    </tr>
                    <tr>
                        <td>401</td>
                        <td>Unauthorized - Authentication required</td>
                    </tr>
                    <tr>
                        <td>403</td>
                        <td>Forbidden - Insufficient permissions</td>
                    </tr>
                    <tr>
                        <td>404</td>
                        <td>Not Found - Resource not found</td>
                    </tr>
                    <tr>
                        <td>500</td>
                        <td>Internal Server Error - Server error</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- RBAC Section -->
        <div class="readme-section">
            <h2>🔐 Role-Based Access Control</h2>

            <h3>Permission Matrix</h3>
            <table>
                <thead>
                    <tr>
                        <th>Feature</th>
                        <th>Admin</th>
                        <th>Editor</th>
                        <th>Reader</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>View Published Posts</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>✅</td>
                    </tr>
                    <tr>
                        <td>View Draft Posts</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Create Posts</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Edit Own Posts</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Edit All Posts</td>
                        <td>✅</td>
                        <td>❌</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Delete Own Posts</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Delete All Posts</td>
                        <td>✅</td>
                        <td>❌</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Manage Users</td>
                        <td>✅</td>
                        <td>❌</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>Manage Categories</td>
                        <td>✅</td>
                        <td>✅</td>
                        <td>❌</td>
                    </tr>
                    <tr>
                        <td>System Settings</td>
                        <td>✅</td>
                        <td>❌</td>
                        <td>❌</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Security Features -->
        <div class="readme-section">
            <h2>🛡️ Security Features</h2>

            <div class="feature-grid">
                <div class="feature-card">
                    <h4>Authentication & Authorization</h4>
                    <ul>
                        <li>JWT token-based authentication</li>
                        <li>Token expiration and refresh mechanism</li>
                        <li>Secure password hashing (bcrypt with salt)</li>
                        <li>Role-based access control (RBAC)</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>Input Validation</h4>
                    <ul>
                        <li>Django form validation</li>
                        <li>Serializer validation in DRF</li>
                        <li>SQL injection prevention (ORM)</li>
                        <li>XSS protection</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>API Security</h4>
                    <ul>
                        <li>CSRF token protection</li>
                        <li>CORS configuration</li>
                        <li>Rate limiting (Django Ratelimit)</li>
                        <li>HTTPS enforcement in production</li>
                    </ul>
                </div>

                <div class="feature-card">
                    <h4>Database Security</h4>
                    <ul>
                        <li>Prepared statements (ORM)</li>
                        <li>Database user with limited privileges</li>
                        <li>Regular backups</li>
                        <li>Encrypted sensitive data</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Future Enhancements -->
        <div class="readme-section">
            <h2>🔮 Future Enhancements</h2>
            <ul>
                <li>Comments System: Add threaded comments with moderation</li>
                <li>Social Sharing: Integrate social media sharing</li>
                <li>Email Notifications: Notify users of new posts</li>
                <li>SEO Optimization: Meta tags, sitemaps, schema markup</li>
                <li>Analytics Dashboard: Track views, engagement metrics</li>
                <li>Content Versioning: Track post history and revisions</li>
                <li>Multi-language Support: Internationalization (i18n)</li>
                <li>Image Optimization: Automatic image compression</li>
                <li>Full-text Search: Implement Elasticsearch</li>
                <li>GraphQL API: Alternative to REST API</li>
            </ul>
        </div>

        <!-- Contact Section -->
        <div class="readme-section">
            <h2>📞 Contact</h2>
            <p><strong>Niha Ruksar</strong></p>
            <p>
                <span class="badge" style="background: #0077B5; color: white;">LinkedIn</span>
                <span class="badge" style="background: #D14836; color: white;">Email</span>
                <span class="badge" style="background: #181717; color: white;">GitHub</span>
                <span class="badge" style="background: #FFA116; color: white;">LeetCode</span>
            </p>
            <p><strong>Project Link:</strong> <a href="https://github.com/NihaRuksar/blogging-platform">https://github.com/NihaRuksar/blogging-platform</a></p>
        </div>

    </div>

    <button class="copy-button" onclick="alert('To take screenshots:\n1. Use your screenshot tool (Win+Shift+S on Windows, Cmd+Shift+4 on Mac)\n2. Capture each screenshot section\n3. Save them as: dashboard.png, post-list.png, post-editor.png, user-management.png, api-response.png\n4. Add to your GitHub repository in a screenshots/ folder')">
        📸 How to Save Screenshots
    </button>
</body>
</html>
---

## 💾 Database Schema
```sql
-- Core Tables

-- Users Table (Extended Django User Model)
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(150) UNIQUE NOT NULL,
    email VARCHAR(254) UNIQUE NOT NULL,
    password VARCHAR(128) NOT NULL,
    role ENUM('admin', 'editor', 'reader') DEFAULT 'reader',
    is_active BOOLEAN DEFAULT TRUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- Blog Posts Table
CREATE TABLE blog_posts (
    id INT PRIMARY KEY AUTO_INCREMENT,
    title VARCHAR(255) NOT NULL,
    slug VARCHAR(255) UNIQUE NOT NULL,
    content TEXT NOT NULL,
    author_id INT NOT NULL,
    status ENUM('draft', 'published', 'archived') DEFAULT 'draft',
    featured_image VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    published_at TIMESTAMP NULL,
    FOREIGN KEY (author_id) REFERENCES users(id) ON DELETE CASCADE,
    INDEX idx_status (status),
    INDEX idx_author (author_id),
    INDEX idx_published (published_at)
);

-- Categories Table
CREATE TABLE categories (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) UNIQUE NOT NULL,
    slug VARCHAR(100) UNIQUE NOT NULL,
    description TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tags Table
CREATE TABLE tags (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50) UNIQUE NOT NULL,
    slug VARCHAR(50) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Many-to-Many Relationships
CREATE TABLE post_categories (
    post_id INT,
    category_id INT,
    PRIMARY KEY (post_id, category_id),
    FOREIGN KEY (post_id) REFERENCES blog_posts(id) ON DELETE CASCADE,
    FOREIGN KEY (category_id) REFERENCES categories(id) ON DELETE CASCADE
);

CREATE TABLE post_tags (
    post_id INT,
    tag_id INT,
    PRIMARY KEY (post_id, tag_id),
    FOREIGN KEY (post_id) REFERENCES blog_posts(id) ON DELETE CASCADE,
    FOREIGN KEY (tag_id) REFERENCES tags(id) ON DELETE CASCADE
);
```

### ER Diagram
```
┌─────────────┐       ┌──────────────┐       ┌─────────────┐
│   Users     │       │  Blog Posts  │       │ Categories  │
├─────────────┤       ├──────────────┤       ├─────────────┤
│ id (PK)     │◄──────┤ id (PK)      │───────┤ id (PK)     │
│ username    │   1:N │ title        │  M:N  │ name        │
│ email       │       │ content      │       │ slug        │
│ role        │       │ author_id FK │       │ description │
│ is_active   │       │ status       │       └─────────────┘
└─────────────┘       │ created_at   │
                      └──────────────┘
                            │
                            │ M:N
                            │
                      ┌─────────────┐
                      │    Tags     │
                      ├─────────────┤
                      │ id (PK)     │
                      │ name        │
                      │ slug        │
                      └─────────────┘
```

---

## 🚀 Installation

### Prerequisites

- Python 3.9 or higher
- MySQL 8.0 or higher
- pip (Python package manager)
- Git

### Step 1: Clone the Repository
```bash
git clone https://github.com/NihaRuksar/blogging-platform.git
cd blogging-platform
```

### Step 2: Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Configure Database

Create a `.env` file in the project root:
```env
# Database Configuration
DB_NAME=blogging_platform
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_HOST=localhost
DB_PORT=3306

# Django Settings
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1

# JWT Settings
JWT_SECRET_KEY=your-jwt-secret-key
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

### Step 5: Create MySQL Database
```bash
mysql -u root -p
```
```sql
CREATE DATABASE blogging_platform CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
EXIT;
```

### Step 6: Run Migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### Step 7: Create Superuser
```bash
python manage.py createsuperuser
```

### Step 8: Load Initial Data (Optional)
```bash
python manage.py loaddata initial_data.json
```

### Step 9: Run Development Server
```bash
python manage.py runserver
```

Visit `http://localhost:8000` to see the application running! 🎉

---

## 📚 API Documentation

### Base URL
```
http://localhost:8000/api/v1/
```

### Authentication

All protected endpoints require JWT token in the header:
```
Authorization: Bearer <your_jwt_token>
```

---

### 🔐 Authentication Endpoints

#### Register User
```http
POST /api/v1/auth/register/
```

**Request Body:**
```json
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "SecurePass123!",
  "role": "reader"
}
```

**Response:**
```json
{
  "id": 1,
  "username": "john_doe",
  "email": "john@example.com",
  "role": "reader",
  "created_at": "2025-03-15T10:30:00Z"
}
```

---

#### Login
```http
POST /api/v1/auth/login/
```

**Request Body:**
```json
{
  "username": "john_doe",
  "password": "SecurePass123!"
}
```

**Response:**
```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "refresh_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "bearer",
  "expires_in": 1800
}
```

---

### 📝 Blog Post Endpoints

#### Get All Posts
```http
GET /api/v1/posts/
```

**Query Parameters:**
- `page` (int): Page number for pagination
- `limit` (int): Items per page (default: 10)
- `status` (string): Filter by status (draft, published, archived)
- `author` (int): Filter by author ID
- `search` (string): Search in title and content

**Response:**
```json
{
  "count": 50,
  "next": "http://localhost:8000/api/v1/posts/?page=2",
  "previous": null,
  "results": [
    {
      "id": 1,
      "title": "Getting Started with Django",
      "slug": "getting-started-with-django",
      "content": "Django is a high-level Python web framework...",
      "author": {
        "id": 1,
        "username": "john_doe",
        "email": "john@example.com"
      },
      "status": "published",
      "featured_image": "/media/posts/django.jpg",
      "categories": [
        {"id": 1, "name": "Web Development", "slug": "web-development"}
      ],
      "tags": [
        {"id": 1, "name": "Django", "slug": "django"},
        {"id": 2, "name": "Python", "slug": "python"}
      ],
      "created_at": "2025-03-15T10:30:00Z",
      "updated_at": "2025-03-16T14:20:00Z",
      "published_at": "2025-03-15T12:00:00Z"
    }
  ]
}
```

---

#### Get Single Post
```http
GET /api/v1/posts/{id}/
```

**Response:** Same as single post object above

---

#### Create Post (Editor/Admin only)
```http
POST /api/v1/posts/
```

**Request Body:**
```json
{
  "title": "Advanced Django Patterns",
  "content": "In this post, we'll explore advanced patterns...",
  "status": "draft",
  "categories": [1, 2],
  "tags": [1, 3, 5]
}
```

**Response:**
```json
{
  "id": 2,
  "title": "Advanced Django Patterns",
  "slug": "advanced-django-patterns",
  "content": "In this post, we'll explore advanced patterns...",
  "author": {
    "id": 1,
    "username": "john_doe"
  },
  "status": "draft",
  "created_at": "2025-03-20T09:15:00Z"
}
```

---



#### Delete Post (Admin only)
```http
DELETE /api/v1/posts/{id}/
```

**Response:**
```json
{
  "message": "Post deleted successfully"
}
```

---

### 📁 Category Endpoints

#### Get All Categories
```http
GET /api/v1/categories/
```

#### Create Category (Admin only)
```http
POST /api/v1/categories/
```

**Request Body:**
```json
{
  "name": "Web Development",
  "description": "Articles about web development"
}
```

---


### 📊 API Response Codes

| Status Code | Meaning |
|------------|---------|
| 200 | OK - Request successful |
| 201 | Created - Resource created successfully |
| 204 | No Content - Resource deleted successfully |
| 400 | Bad Request - Invalid input |
| 401 | Unauthorized - Authentication required |
| 403 | Forbidden - Insufficient permissions |
| 404 | Not Found - Resource not found |
| 500 | Internal Server Error - Server error |

---

### 1. Dashboard Overview
```
- Shows statistics: Total posts, users, categories
- Recent activity feed
- Quick action buttons
```

---

### 2. Blog Post List
```
- Table/grid view of all blog posts
- Filter and search functionality
- Status indicators (draft/published)
- Action buttons (edit/delete)
```

---

### 3. Create/Edit Post Interface
```
- Rich text editor
- Category and tag selection
- Image upload
- Draft/Publish options
```

---

### 4. User Management (Admin)
```
- User list with roles
- Add/edit user interface
- Role assignment dropdown
```

---

### 5. API Response (Postman)
```
- GET request to /api/v1/posts/
- JSON response with post data
- Headers showing JWT token
```

---

## 🔐 Role-Based Access Control

### Permission Matrix

| Feature | Admin | Editor | Reader |
|---------|-------|--------|--------|
| View Published Posts | ✅ | ✅ | ✅ |
| View Draft Posts | ✅ | ✅ | ❌ |
| Create Posts | ✅ | ✅ | ❌ |
| Edit Own Posts | ✅ | ✅ | ❌ |
| Edit All Posts | ✅ | ❌ | ❌ |
| Delete Own Posts | ✅ | ✅ | ❌ |
| Delete All Posts | ✅ | ❌ | ❌ |
| Manage Users | ✅ | ❌ | ❌ |
| Manage Categories | ✅ | ✅ | ❌ |
| Manage Tags | ✅ | ✅ | ❌ |
| System Settings | ✅ | ❌ | ❌ |

### Implementation
```python
# Example permission class in Django
from rest_framework.permissions import BasePermission

class IsAdminOrReadOnly(BasePermission):
    def has_permission(self, request, view):
        if request.method in ['GET', 'HEAD', 'OPTIONS']:
            return True
        return request.user and request.user.role == 'admin'

class IsEditorOrAdmin(BasePermission):
    def has_permission(self, request, view):
        return request.user and request.user.role in ['admin', 'editor']
    
    def has_object_permission(self, request, view, obj):
        if request.user.role == 'admin':
            return True
        return obj.author == request.user
```


- ✅ SQL injection prevention (ORM)
- ✅ XSS protection





