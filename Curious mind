<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Curious Minds - Explore, Learn, Discover</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f4f4f4;
        }

        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 2rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .tagline {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .admin-btn {
            padding: 0.8rem 1.5rem;
            background: rgba(255,255,255,0.2);
            color: white;
            border: 2px solid white;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .admin-btn:hover {
            background: white;
            color: #667eea;
        }

        .main-content {
            padding: 2rem 0;
        }

        .posts {
            display: grid;
            gap: 2rem;
            max-width: 900px;
            margin: 0 auto;
        }

        .post-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .post-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        .post-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .post-content {
            padding: 1.5rem;
        }

        .post-meta {
            display: flex;
            gap: 1rem;
            margin-bottom: 1rem;
            font-size: 0.9rem;
            color: #666;
            flex-wrap: wrap;
        }

        .post-title {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .post-excerpt {
            color: #666;
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        .read-more, .edit-btn, .delete-btn {
            display: inline-block;
            padding: 0.5rem 1.2rem;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s;
            border: none;
            cursor: pointer;
            font-size: 0.9rem;
            margin-right: 0.5rem;
            margin-top: 0.5rem;
        }

        .read-more {
            background: #667eea;
        }

        .read-more:hover {
            background: #764ba2;
        }

        .edit-btn {
            background: #4CAF50;
        }

        .edit-btn:hover {
            background: #45a049;
        }

        .delete-btn {
            background: #f44336;
        }

        .delete-btn:hover {
            background: #da190b;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 1000;
            overflow-y: auto;
        }

        .modal-content {
            background: white;
            max-width: 800px;
            margin: 2rem auto;
            padding: 2rem;
            border-radius: 10px;
            position: relative;
        }

        .close-modal {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 2rem;
            cursor: pointer;
            color: #666;
            background: none;
            border: none;
        }

        .close-modal:hover {
            color: #333;
        }

        .admin-panel {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            margin: 2rem auto;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            max-width: 800px;
        }

        .admin-panel h2 {
            color: #667eea;
            margin-bottom: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: #333;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            font-family: inherit;
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        .btn-primary, .btn-secondary {
            padding: 0.8rem 2rem;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s;
        }

        .btn-primary {
            background: #667eea;
        }

        .btn-primary:hover {
            background: #764ba2;
        }

        .btn-secondary {
            background: #6c757d;
            margin-left: 0.5rem;
        }

        .btn-secondary:hover {
            background: #5a6268;
        }

        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        .empty-state {
            text-align: center;
            padding: 3rem;
            color: #666;
            background: white;
            border-radius: 10px;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div>
                    <h1>🧠 Curious Minds</h1>
                    <p class="tagline">by Sarthak Nayyar</p>
                    <p class="tagline" style="margin-top: 0.3rem;">Explore, Learn, Discover</p>
                </div>
                <div>
                    <button class="admin-btn" id="toggleBtn">✏️ Write Post</button>
                    <button class="admin-btn" onclick="if(confirm('Reset blog and load 5 sample posts?')) { localStorage.clear(); location.reload(); }" style="margin-left: 0.5rem;">🔄 Reset Blog</button>
                </div>
            </div>
        </div>
    </header>

    <!-- Home Page -->
    <div id="homePage" class="page active">
        <div class="container">
            <div class="main-content">
                <div class="posts" id="postsContainer"></div>
            </div>
        </div>
    </div>

    <!-- Admin Page -->
    <div id="adminPage" class="page">
        <div class="container">
            <div class="admin-panel">
                <h2 id="formTitle">Create New Post</h2>
                
                <div class="form-group">
                    <label>Post Title *</label>
                    <input type="text" id="title">
                </div>

                <div class="form-group">
                    <label>Excerpt / Summary *</label>
                    <textarea id="excerpt"></textarea>
                </div>

                <div class="form-group">
                    <label>Full Content *</label>
                    <textarea id="content" style="min-height: 250px;"></textarea>
                </div>

                <div class="form-group">
                    <label>Category *</label>
                    <select id="category">
                        <option value="science">Science</option>
                        <option value="technology">Technology</option>
                        <option value="philosophy">Philosophy</option>
                        <option value="culture">Culture</option>
                    </select>
                </div>

                <div class="form-group">
                    <label>Icon (emoji)</label>
                    <input type="text" id="icon" value="📝">
                </div>

                <div class="form-group">
                    <label>Author Name *</label>
                    <input type="text" id="author" value="Sarthak Nayyar">
                </div>

                <button class="btn-primary" id="publishBtn">Publish Post</button>
                <button class="btn-secondary" id="cancelBtn">Cancel</button>
                <button class="btn-secondary" onclick="console.log('Total posts:', posts); alert('You have ' + posts.length + ' posts');" style="margin-left: 0.5rem;">Check Posts</button>
            </div>
        </div>
    </div>

    <!-- Post Modal -->
    <div id="postModal" class="modal">
        <div class="modal-content">
            <button class="close-modal" id="closeModalBtn">&times;</button>
            <div id="modalBody"></div>
        </div>
    </div>

    <script>
        const DB_KEY = 'curiousMindsPosts';
        let posts = [];
        let editingId = null;
        let showingAdmin = false;

        // Load posts from storage
        function loadPosts() {
            // Force load sample posts for now
            posts = [
                {
                    id: 1,
                    title: "Welcome to Curious Minds!",
                    excerpt: "Your journey into fascinating ideas begins here. Edit this post or create your own content to share with the world.",
                    content: "Welcome to Curious Minds! This is your personal blog space where you can share thoughts, ideas, and knowledge. Click the 'Edit' button below any post to customize it with your own content. Each post can include your unique perspective on science, technology, philosophy, culture, or any topic that sparks your curiosity.",
                    category: "culture",
                    icon: "👋",
                    author: "Sarthak Nayyar",
                    date: "Jan 9, 2026"
                },
                {
                    id: 2,
                    title: "Why Is the Sky Dark at Night?",
                    excerpt: "If the universe is filled with billions of stars, why isn't the entire night sky bright? Discover the fascinating answer to this cosmic mystery.",
                    content: "When we look up at the night sky, it appears mostly dark, with only a few bright points of light coming from stars. This feels normal to us, but if we stop and think about it, it becomes a very interesting question. The universe contains billions of stars and galaxies. If there are so many stars in every direction, then why isn't the entire night sky bright? Why do we see darkness instead of light everywhere?\n\nAt first, it seems logical to expect the sky to be bright. If the universe were filled with stars in all directions, then no matter where we looked, our eyes should eventually land on the surface of a star. In that case, the sky should glow continuously, just like the surface of the Sun. This idea confused scientists for a long time and became a famous problem in astronomy.\n\nThe main reason the sky is dark at night is that the universe is not infinitely old. The universe had a beginning, often called the Big Bang, which happened about 13.8 billion years ago. Light takes time to travel through space. This means we can only see light from stars and galaxies whose light has had enough time to reach Earth. There are many stars that are so far away that their light has not reached us yet. Because of this, large parts of the sky remain dark.\n\nAnother important reason is that the universe is expanding. As the universe expands, distant galaxies move away from us. The light coming from very far galaxies gets stretched as it travels through space. This stretching reduces the energy of the light, making it weaker and sometimes invisible to our eyes. As a result, even though stars exist in those regions, their light does not brighten the night sky.\n\nDust and gas in space also play a small role. Some light from distant stars is absorbed or scattered by interstellar matter before it reaches us. However, this is not the main reason for the dark sky. The biggest reasons are the finite age of the universe and the expansion of space itself.\n\nThis question is sometimes called Olbers' Paradox, named after a scientist who studied this problem. The solution to this paradox helped scientists understand that the universe is not eternal and unchanging, but dynamic and evolving.\n\nIn conclusion, the sky is dark at night because the universe has a limited age, light takes time to travel, and space is constantly expanding. Even though the universe is filled with stars, we can only see a small portion of them. The darkness of the night sky is not empty at all — it is evidence of the vast size and fascinating nature of the universe.",
                    category: "science",
                    icon: "🌌",
                    author: "Sarthak Nayyar",
                    date: "Jan 8, 2026"
                },
                {
                    id: 3,
                    title: "What Is Time Dilation? A Simple Explanation for Students",
                    excerpt: "Time is not the same for everyone. Discover how Einstein's theory of relativity changed our understanding of time and why astronauts age slower than people on Earth.",
                    content: "Time is something we all experience every day. We use clocks to measure it and we usually think that time moves at the same speed for everyone. One second for me is one second for you — or at least that's what we naturally believe. For a long time, scientists also believed that time was absolute and the same everywhere. But this idea changed in the early 20th century because of Albert Einstein.\n\nTime dilation is a concept that comes from Einstein's theory of relativity. In simple words, time dilation means that time does not pass at the same rate for everyone. The speed at which time flows depends on how fast a person is moving or how strong gravity is around them. This idea sounds strange at first, but it has been proven by experiments.\n\nOne easy way to understand time dilation is by imagining a very fast-moving object, like a spaceship. Suppose an astronaut travels in a spaceship that moves close to the speed of light, while another person stays on Earth. For the astronaut, time moves normally — their watch ticks one second at a time. But for the person on Earth, the astronaut's clock appears to move slower. When the astronaut returns, they would be younger than the person who stayed on Earth. This difference in time is called time dilation.\n\nTime dilation happens because the speed of light is constant for everyone. No matter how fast someone moves, the speed of light remains the same. To make this possible, time itself adjusts. When something moves very fast, time slows down for it compared to someone who is not moving as fast.\n\nThis effect is not just a theory. It is used in real life. GPS satellites, for example, experience time differently because they move fast and are far from Earth's gravity. Scientists must correct time dilation effects, otherwise GPS locations would become inaccurate.\n\nIn conclusion, time dilation shows that time is not absolute. It changes depending on motion and gravity. Even though we don't notice it in daily life, it becomes very important at high speeds and in space. This idea completely changed how scientists understand time and the universe.",
                    category: "science",
                    icon: "⏰",
                    author: "Sarthak Nayyar",
                    date: "Jan 7, 2026"
                },
                {
                    id: 4,
                    title: "Is the Universe Expanding Into Something?",
                    excerpt: "If the universe is expanding, what is it expanding into? The answer to this question is far stranger than you might expect.",
                    content: "When we hear that the universe is expanding, a natural question comes to mind: expanding into what? If everything is growing and moving away from each other, it feels logical to imagine the universe spreading into some empty space beyond it. But modern physics gives a very surprising answer to this question.\n\nTo understand this, we first need to clarify what scientists mean by an \"expanding universe.\" The expansion of the universe does not mean that galaxies are flying outward from a central point into empty space. Instead, it means that the space between galaxies is increasing. Imagine drawing dots on the surface of a balloon. As the balloon inflates, the dots move farther apart, even though they are not moving on the surface themselves. There is no center on the surface of the balloon — everything simply moves away from everything else.\n\nSimilarly, the universe does not need to expand into anything. Space itself is stretching. Galaxies remain mostly in the same locations, but the distance between them increases over time. This is why distant galaxies appear to be moving away from us, and the farther they are, the faster they seem to recede.\n\nOne of the strongest pieces of evidence for this expansion comes from the light we receive from distant galaxies. This light is stretched as it travels through expanding space, a phenomenon called redshift. The more stretched the light is, the farther away the galaxy is. This observation shows that space has been expanding for billions of years.\n\nSo, is there an \"outside\" of the universe? As far as current science tells us, there is no known edge or outside space that the universe is expanding into. The universe includes all of space itself. Asking what it is expanding into is similar to asking what lies north of the North Pole — the question sounds reasonable, but it does not apply within the structure of the system.\n\nThis idea can feel uncomfortable because our brains are used to thinking in terms of objects expanding into empty space. However, the universe does not behave like everyday objects. Space is not something that exists inside a larger container; it is the container itself.\n\nIn conclusion, the universe is expanding, but not into anything. Space itself is growing, stretching the distances between galaxies. While this concept is difficult to imagine, it is supported by strong observations and forms a key part of our understanding of the universe. The expansion of the universe reminds us that reality is often far stranger than our everyday intuition suggests.",
                    category: "science",
                    icon: "🌌",
                    author: "Sarthak Nayyar",
                    date: "Jan 6, 2026"
                },
                {
                    id: 5,
                    title: "The Power of Creative Thinking",
                    excerpt: "Creativity isn't just for artists - it's a crucial skill for problem-solving and innovation in every field.",
                    content: "Creative thinking drives innovation across all domains. Whether you're an engineer, scientist, writer, or entrepreneur, creativity helps you see new possibilities and solve complex problems. Edit this post to share your thoughts on creativity, innovation, or any topic that inspires you. What creative projects are you working on?",
                    category: "culture",
                    icon: "💡",
                    author: "Sarthak Nayyar",
                    date: "Jan 5, 2026"
                }
            ];
        }

        // Save posts to storage
        function savePosts() {
            try {
                const jsonString = JSON.stringify(posts);
                localStorage.setItem(DB_KEY, jsonString);
                console.log('Successfully saved', posts.length, 'posts to localStorage');
                console.log('Posts array:', posts);
            } catch (error) {
                console.error('ERROR saving to localStorage:', error);
                alert('Error saving posts: ' + error.message);
            }
        }

        // Render all posts
        function render() {
            const container = document.getElementById('postsContainer');
            
            if (posts.length === 0) {
                container.innerHTML = '<div class="empty-state"><h3>No posts yet</h3><p>Click Write Post to create one!</p></div>';
                return;
            }

            container.innerHTML = posts.map(p => `
                <article class="post-card">
                    <div class="post-image">${p.icon}</div>
                    <div class="post-content">
                        <div class="post-meta">
                            <span>📅 ${p.date}</span>
                            <span>✍️ ${p.author}</span>
                            <span>📂 ${p.category}</span>
                        </div>
                        <h2 class="post-title">${p.title}</h2>
                        <p class="post-excerpt">${p.excerpt}</p>
                        <div>
                            <button class="read-more" onclick="viewPost(${p.id})">Read More →</button>
                            <button class="edit-btn" onclick="editPost(${p.id})">Edit</button>
                            <button class="delete-btn" onclick="deletePost(${p.id})">Delete</button>
                        </div>
                    </div>
                </article>
            `).join('');
        }

        // Toggle between home and admin
        function toggleView() {
            showingAdmin = !showingAdmin;
            document.getElementById('homePage').classList.toggle('active', !showingAdmin);
            document.getElementById('adminPage').classList.toggle('active', showingAdmin);
            document.getElementById('toggleBtn').textContent = showingAdmin ? '📖 View Blog' : '✏️ Write Post';
            window.scrollTo(0, 0);
        }

        // Clear form
        function clearForm() {
            document.getElementById('title').value = '';
            document.getElementById('excerpt').value = '';
            document.getElementById('content').value = '';
            document.getElementById('category').value = 'science';
            document.getElementById('icon').value = '📝';
            document.getElementById('author').value = 'Sarthak Nayyar';
            document.getElementById('formTitle').textContent = 'Create New Post';
            editingId = null;
        }

        // Publish post
        function publishPost() {
            console.log('=== STARTING PUBLISH ===');
            try {
                console.log('Step 1: Getting form values...');
                
                const title = document.getElementById('title').value.trim();
                const excerpt = document.getElementById('excerpt').value.trim();
                const content = document.getElementById('content').value.trim();
                const category = document.getElementById('category').value;
                const icon = document.getElementById('icon').value.trim() || '📝';
                const author = document.getElementById('author').value.trim();

                console.log('Step 2: Form values retrieved');
                console.log('- Title:', title);
                console.log('- Excerpt length:', excerpt.length);
                console.log('- Content length:', content.length);
                console.log('- Author:', author);

                if (!title) {
                    alert('Please enter a title!');
                    return;
                }
                if (!excerpt) {
                    alert('Please enter an excerpt!');
                    return;
                }
                if (!content) {
                    alert('Please enter content!');
                    return;
                }
                if (!author) {
                    alert('Please enter author name!');
                    return;
                }

                console.log('Step 3: All validations passed');
                console.log('Step 4: Current posts count BEFORE adding:', posts.length);

                const post = {
                    id: editingId || Date.now(),
                    title: title,
                    excerpt: excerpt,
                    content: content,
                    category: category,
                    icon: icon,
                    author: author,
                    date: new Date().toLocaleDateString('en-US', { month: 'short', day: 'numeric', year: 'numeric' })
                };

                console.log('Step 5: Post object created with ID:', post.id);

                if (editingId) {
                    console.log('Step 6a: Editing existing post');
                    const idx = posts.findIndex(p => p.id === editingId);
                    posts[idx] = post;
                } else {
                    console.log('Step 6b: Adding NEW post');
                    posts.unshift(post);
                }

                console.log('Step 7: Posts count AFTER adding:', posts.length);
                
                console.log('Step 8: Calling savePosts()...');
                savePosts();
                
                console.log('Step 9: Calling render()...');
                render();
                
                console.log('Step 10: Calling clearForm()...');
                clearForm();
                
                console.log('Step 11: Calling toggleView()...');
                toggleView();
                
                console.log('Step 12: Showing success alert...');
                alert('✅ Post published successfully! You now have ' + posts.length + ' posts.');
                
                console.log('=== PUBLISH COMPLETE ===');
                
            } catch (error) {
                console.error('!!! ERROR in publishPost:', error);
                console.error('Error stack:', error.stack);
                alert('Error: ' + error.message);
            }
        }

        // Edit post
        function editPost(id) {
            const post = posts.find(p => p.id === id);
            if (!post) return;

            editingId = id;
            document.getElementById('title').value = post.title;
            document.getElementById('excerpt').value = post.excerpt;
            document.getElementById('content').value = post.content;
            document.getElementById('category').value = post.category;
            document.getElementById('icon').value = post.icon;
            document.getElementById('author').value = post.author;
            document.getElementById('formTitle').textContent = 'Edit Post';

            if (!showingAdmin) toggleView();
        }

        // Delete post
        function deletePost(id) {
            if (!confirm('Delete this post?')) return;
            posts = posts.filter(p => p.id !== id);
            savePosts();
            render();
        }

        // View post in modal
        function viewPost(id) {
            const post = posts.find(p => p.id === id);
            if (!post) return;

            document.getElementById('modalBody').innerHTML = `
                <div class="post-image" style="height: 200px; border-radius: 10px; margin-bottom: 2rem;">${post.icon}</div>
                <div class="post-meta" style="margin-bottom: 1rem;">
                    <span>📅 ${post.date}</span>
                    <span>✍️ ${post.author}</span>
                    <span>📂 ${post.category}</span>
                </div>
                <h2 style="font-size: 2rem; margin-bottom: 1.5rem;">${post.title}</h2>
                <div style="font-size: 1.1rem; line-height: 1.8; white-space: pre-wrap;">${post.content}</div>
            `;
            document.getElementById('postModal').style.display = 'block';
        }

        // Close modal
        function closeModal() {
            document.getElementById('postModal').style.display = 'none';
        }

        // Event listeners
        document.getElementById('toggleBtn').addEventListener('click', toggleView);
        document.getElementById('publishBtn').addEventListener('click', publishPost);
        document.getElementById('cancelBtn').addEventListener('click', () => {
            clearForm();
            toggleView();
        });
        document.getElementById('closeModalBtn').addEventListener('click', closeModal);
        document.getElementById('postModal').addEventListener('click', (e) => {
            if (e.target.id === 'postModal') closeModal();
        });

        // Initialize
        loadPosts();
        render();
    </script>
</body>
</html>
