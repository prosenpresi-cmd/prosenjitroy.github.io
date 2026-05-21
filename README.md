
/*
README.md

# Prosenjit Roy Academic Website

This is a personal academic homepage for Prosenjit Roy.

## Features

- Research interests
- Publications section
- Teaching section
- Contact information
- Responsive modern design

## How to Use

1. Create a GitHub repository named:

   prosenjitroy.github.io

2. Upload this project.

3. Enable GitHub Pages:

   Settings → Pages → Deploy from branch → main

4. Your website will appear at:

   https://prosenjitroy.github.io

## Customization

You can edit:

- publications
- email
- profile links
- photograph
- research interests

## Technologies

- React
- Tailwind CSS

*/

export default function ProsenjitRoyHomepage() {
  const publications = [
    {
      title: "Singular Moser–Trudinger inequalities and extremals",
      journal: "Journal Article",
      year: "2024",
    },
    {
      title: "Fractional Hardy inequalities and applications",
      journal: "Preprint",
      year: "2025",
    },
    {
      title: "Weak Lp estimates in nonlinear PDE",
      journal: "Research Article",
      year: "2025",
    },
  ];

  const courses = [
    "Functional Analysis",
    "Partial Differential Equations",
    "Real Analysis",
    "Sobolev Spaces and Applications",
  ];

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Header */}
      <header className="bg-white shadow-sm border-b">
        <div className="max-w-6xl mx-auto px-6 py-8 flex flex-col md:flex-row md:items-center md:justify-between gap-4">
          <div>
            <h1 className="text-4xl font-bold tracking-tight">Prosenjit Roy</h1>
            <p className="text-lg text-gray-600 mt-2">
              Department of Mathematics and Statistics
            </p>
            <p className="text-gray-600">Indian Institute of Technology Kanpur</p>
          </div>

          <nav className="flex flex-wrap gap-4 text-sm font-medium">
            <a href="#about" className="hover:text-blue-700">About</a>
            <a href="#research" className="hover:text-blue-700">Research</a>
            <a href="#publications" className="hover:text-blue-700">Publications</a>
            <a href="#teaching" className="hover:text-blue-700">Teaching</a>
            <a href="#contact" className="hover:text-blue-700">Contact</a>
          </nav>
        </div>
      </header>

      {/* Hero */}
      <section className="max-w-6xl mx-auto px-6 py-16 grid md:grid-cols-3 gap-10 items-center">
        <div className="md:col-span-1 flex justify-center">
          <div className="w-64 h-64 rounded-3xl bg-gray-200 flex items-center justify-center shadow-lg text-gray-500 text-lg">
            Your Photo
          </div>
        </div>

        <div className="md:col-span-2 space-y-6">
          <div>
            <h2 className="text-3xl font-semibold mb-4">Research Interests</h2>
            <p className="text-lg leading-8 text-gray-700">
              Nonlinear partial differential equations, Sobolev inequalities,
              Moser–Trudinger type inequalities, weak Lp spaces, nonlocal PDE,
              variational methods, and asymptotic analysis.
            </p>
          </div>

          <div className="flex flex-wrap gap-4">
            <a
              href="https://scholar.google.com"
              className="px-5 py-3 rounded-2xl bg-black text-white hover:opacity-90 transition"
            >
              Google Scholar
            </a>

            <a
              href="https://arxiv.org"
              className="px-5 py-3 rounded-2xl bg-white border hover:bg-gray-100 transition"
            >
              arXiv
            </a>

            <a
              href="https://www.iitk.ac.in/prosenjit-roy"
              className="px-5 py-3 rounded-2xl bg-white border hover:bg-gray-100 transition"
            >
              IIT Kanpur Profile
            </a>
          </div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="max-w-6xl mx-auto px-6 py-12">
        <div className="bg-white rounded-3xl shadow-sm p-8">
          <h2 className="text-3xl font-semibold mb-6">About</h2>
          <p className="text-gray-700 leading-8 text-lg">
            I am a mathematician working in analysis and nonlinear partial
            differential equations. My research focuses on critical embedding
            phenomena, Hardy-type inequalities, weak function spaces, and
            variational techniques arising in elliptic and nonlocal equations.
          </p>
        </div>
      </section>

      {/* Research */}
      <section id="research" className="max-w-6xl mx-auto px-6 py-12">
        <h2 className="text-3xl font-semibold mb-8">Current Research Themes</h2>

        <div className="grid md:grid-cols-2 gap-6">
          {[
            "Moser–Trudinger inequalities",
            "Weak Lp and Lorentz spaces",
            "Fractional elliptic equations",
            "Critical Sobolev embeddings",
            "Variational methods",
            "Nonlocal PDE and asymptotic analysis",
          ].map((item) => (
            <div
              key={item}
              className="bg-white rounded-2xl shadow-sm p-6 border"
            >
              <p className="text-lg font-medium">{item}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Publications */}
      <section id="publications" className="max-w-6xl mx-auto px-6 py-12">
        <h2 className="text-3xl font-semibold mb-8">Selected Publications</h2>

        <div className="space-y-5">
          {publications.map((pub, idx) => (
            <div
              key={idx}
              className="bg-white rounded-2xl p-6 shadow-sm border"
            >
              <div className="flex flex-col md:flex-row md:justify-between gap-2">
                <div>
                  <h3 className="text-xl font-semibold">{pub.title}</h3>
                  <p className="text-gray-600 mt-2">{pub.journal}</p>
                </div>

                <div className="text-gray-500 font-medium">{pub.year}</div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Teaching */}
      <section id="teaching" className="max-w-6xl mx-auto px-6 py-12">
        <h2 className="text-3xl font-semibold mb-8">Teaching</h2>

        <div className="grid md:grid-cols-2 gap-5">
          {courses.map((course) => (
            <div
              key={course}
              className="bg-white rounded-2xl border p-6 shadow-sm"
            >
              <p className="text-lg">{course}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="max-w-6xl mx-auto px-6 py-12">
        <div className="bg-black text-white rounded-3xl p-10">
          <h2 className="text-3xl font-semibold mb-6">Contact</h2>

          <div className="space-y-3 text-lg text-gray-300">
            <p>Department of Mathematics and Statistics</p>
            <p>Indian Institute of Technology Kanpur</p>
            <p>Kanpur, India</p>
            <p>Email: your-email@iitk.ac.in</p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-10 text-center text-gray-500 text-sm">
        © 2026 Prosenjit Roy
      </footer>
    </div>
  );
}
