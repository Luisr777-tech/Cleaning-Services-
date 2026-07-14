export default function CleaningCompanyWebsite() { const company = { name: "Prime Building Cleaning", slogan: "Professional Commercial Cleaning Services", phone: "+1 (317) 555-9812", whatsapp: "https://wa.me/13175559812", email: "info@primebuildingcleaning.com", careersEmail: "careers@primebuildingcleaning.com", address: "Indianapolis, Indiana, USA", };

const services = [ { title: "Commercial Building Cleaning", description: "Complete cleaning solutions for office buildings, business centers, and commercial properties.", image: "https://images.unsplash.com/photo-1520607162513-77705c0f0d4a?q=80&w=1200&auto=format&fit=crop", }, { title: "Office Deep Cleaning", description: "Detailed sanitization and maintenance for professional work environments.", image: "https://images.unsplash.com/photo-1581578731548-c64695cc6952?q=80&w=1200&auto=format&fit=crop", }, { title: "Industrial Maintenance", description: "Reliable cleaning support for industrial and warehouse facilities.", image: "https://images.unsplash.com/photo-1600566752355-35792bedcfea?q=80&w=1200&auto=format&fit=crop", }, ];

const testimonials = [ { name: "Michael Carter", text: "Outstanding service. Their team keeps our office spotless every week.", }, { name: "Sarah Williams", text: "Professional, reliable, and always on time. Highly recommended.", }, { name: "Daniel Roberts", text: "The quality of their commercial cleaning exceeded our expectations.", }, ];

const careers = [ "Commercial Cleaner", "Building Maintenance Technician", "Janitorial Supervisor", "Floor Care Specialist", ];

return ( <div className="bg-white text-gray-800 font-sans"> {/* HERO SECTION */} <section className="relative h-screen bg-cover bg-center flex items-center justify-center" style={{ backgroundImage: "url('https://images.unsplash.com/photo-1521791136064-7986c2920216?q=80&w=1600&auto=format&fit=crop')", }} > <div className="absolute inset-0 bg-black/60"></div>

<div className="relative z-10 text-center max-w-4xl px-6 text-white">
      <h1 className="text-5xl md:text-7xl font-bold leading-tight mb-6">
        {company.name}
      </h1>

      <p className="text-xl md:text-2xl text-gray-200 mb-8">
        {company.slogan}
      </p>

      <div className="flex flex-wrap justify-center gap-4">
        <a
          href={company.whatsapp}
          target="_blank"
          className="bg-green-500 hover:bg-green-600 transition px-6 py-4 rounded-2xl text-lg font-semibold shadow-lg"
        >
          WhatsApp Us
        </a>

        <a
          href={`mailto:${company.email}`}
          className="bg-white text-black hover:bg-gray-200 transition px-6 py-4 rounded-2xl text-lg font-semibold shadow-lg"
        >
          Email Us
        </a>

        <a
          href="#reviews"
          className="border border-white hover:bg-white hover:text-black transition px-6 py-4 rounded-2xl text-lg font-semibold"
        >
          Customer Reviews
        </a>
      </div>
    </div>
  </section>

  {/* ABOUT */}
  <section className="py-24 px-6 md:px-20 bg-gray-50">
    <div className="max-w-6xl mx-auto grid md:grid-cols-2 gap-14 items-center">
      <div>
        <h2 className="text-4xl font-bold mb-6">
          Professional Cleaning You Can Trust
        </h2>

        <p className="text-lg leading-8 text-gray-600 mb-6">
          We provide premium commercial cleaning services designed for office buildings,
          business facilities, medical offices, and industrial spaces.
        </p>

        <p className="text-lg leading-8 text-gray-600">
          Our experienced team focuses on reliability, safety, detailed cleaning, and
          professional customer care.
        </p>
      </div>

      <img
        src="https://images.unsplash.com/photo-1527515637462-cff94eecc1ac?q=80&w=1200&auto=format&fit=crop"
        alt="Cleaning team"
        className="rounded-3xl shadow-2xl h-[500px] w-full object-cover"
      />
    </div>
  </section>

  {/* SERVICES */}
  <section className="py-24 px-6 md:px-20 bg-white">
    <div className="max-w-7xl mx-auto">
      <div className="text-center mb-16">
        <h2 className="text-4xl font-bold mb-4">Our Services</h2>
        <p className="text-lg text-gray-600">
          Professional cleaning solutions tailored for your business.
        </p>
      </div>

      <div className="grid md:grid-cols-3 gap-10">
        {services.map((service, index) => (
          <div
            key={index}
            className="bg-gray-50 rounded-3xl overflow-hidden shadow-lg hover:shadow-2xl transition"
          >
            <img
              src={service.image}
              alt={service.title}
              className="h-64 w-full object-cover"
            />

            <div className="p-8">
              <h3 className="text-2xl font-bold mb-4">{service.title}</h3>
              <p className="text-gray-600 leading-7">{service.description}</p>
            </div>
          </div>
        ))}
      </div>
    </div>
  </section>

  {/* WHY CHOOSE US */}
  <section className="py-24 px-6 md:px-20 bg-gray-900 text-white">
    <div className="max-w-6xl mx-auto text-center">
      <h2 className="text-4xl font-bold mb-12">Why Choose Us</h2>

      <div className="grid md:grid-cols-4 gap-8">
        <div className="bg-white/10 rounded-3xl p-8 backdrop-blur-sm">
          <h3 className="text-2xl font-bold mb-3">Reliable</h3>
          <p className="text-gray-300">
            Consistent service with dependable scheduling.
          </p>
        </div>

        <div className="bg-white/10 rounded-3xl p-8 backdrop-blur-sm">
          <h3 className="text-2xl font-bold mb-3">Professional</h3>
          <p className="text-gray-300">
            Trained teams delivering top-quality cleaning.
          </p>
        </div>

        <div className="bg-white/10 rounded-3xl p-8 backdrop-blur-sm">
          <h3 className="text-2xl font-bold mb-3">Flexible</h3>
          <p className="text-gray-300">
            Customized plans for every business size.
          </p>
        </div>

        <div className="bg-white/10 rounded-3xl p-8 backdrop-blur-sm">
          <h3 className="text-2xl font-bold mb-3">Safe</h3>
          <p className="text-gray-300">
            Eco-friendly products and secure cleaning standards.
          </p>
        </div>
      </div>
    </div>
  </section>

  {/* REVIEWS */}
  <section id="reviews" className="py-24 px-6 md:px-20 bg-gray-50">
    <div className="max-w-6xl mx-auto text-center">
      <h2 className="text-4xl font-bold mb-4">Customer Reviews</h2>
      <p className="text-lg text-gray-600 mb-14">
        What our clients say about our cleaning services.
      </p>

      <div className="grid md:grid-cols-3 gap-8">
        {testimonials.map((review, index) => (
          <div
            key={index}
            className="bg-white rounded-3xl shadow-lg p-8 text-left"
          >
            <div className="text-yellow-500 text-2xl mb-4">★★★★★</div>
            <p className="text-gray-600 leading-7 mb-6">“{review.text}”</p>
            <h4 className="font-bold text-lg">{review.name}</h4>
          </div>
        ))}
      </div>
    </div>
  </section>

  {/* CAREERS */}
  <section className="py-24 px-6 md:px-20 bg-white">
    <div className="max-w-6xl mx-auto grid md:grid-cols-2 gap-14 items-center">
      <div>
        <h2 className="text-4xl font-bold mb-6">Careers</h2>

        <p className="text-lg text-gray-600 leading-8 mb-8">
          Join our growing cleaning team. We are always looking for motivated,
          professional, and reliable people.
        </p>

        <div className="space-y-4 mb-8">
          {careers.map((job, index) => (
            <div
              key={index}
              className="border border-gray-200 rounded-2xl px-6 py-4 flex justify-between items-center"
            >
              <span className="font-medium">{job}</span>
              <span className="text-green-600 font-semibold">Open</span>
            </div>
          ))}
        </div>

        <a
          href={`mailto:${company.careersEmail}`}
          className="inline-block bg-black text-white px-8 py-4 rounded-2xl font-semibold hover:bg-gray-800 transition"
        >
          Apply by Email
        </a>
      </div>

      <img
        src="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?q=80&w=1200&auto=format&fit=crop"
        alt="Careers"
        className="rounded-3xl shadow-2xl h-[500px] object-cover w-full"
      />
    </div>
  </section>

  {/* CONTACT */}
  <section className="py-24 px-6 md:px-20 bg-gray-100">
    <div className="max-w-5xl mx-auto bg-white rounded-3xl shadow-2xl p-10 md:p-16">
      <div className="text-center mb-12">
        <h2 className="text-4xl font-bold mb-4">Contact Us</h2>
        <p className="text-lg text-gray-600">
          Request a quote or contact our team today.
        </p>
      </div>

      <div className="grid md:grid-cols-2 gap-12">
        <div className="space-y-6">
          <div>
            <h3 className="font-bold text-xl mb-2">Phone</h3>
            <p className="text-gray-600">{company.phone}</p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-2">Email</h3>
            <p className="text-gray-600">{company.email}</p>
          </div>

          <div>
            <h3 className="font-bold text-xl mb-2">Location</h3>
            <p className="text-gray-600">{company.address}</p>
          </div>
        </div>

        <form className="space-y-5">
          <input
            type="text"
            placeholder="Full Name"
            className="w-full border border-gray-300 rounded-2xl px-5 py-4"
          />

          <input
            type="email"
            placeholder="Email Address"
            className="w-full border border-gray-300 rounded-2xl px-5 py-4"
          />

          <textarea
            rows="5"
            placeholder="Write your message..."
            className="w-full border border-gray-300 rounded-2xl px-5 py-4"
          ></textarea>

          <button
            type="submit"
            className="w-full bg-green-600 hover:bg-green-700 transition text-white py-4 rounded-2xl font-semibold text-lg"
          >
            Send Message
          </button>
        </form>
      </div>
    </div>
  </section>

  {/* FOOTER */}
  <footer className="bg-black text-white py-10 px-6 md:px-20">
    <div className="max-w-7xl mx-auto flex flex-col md:flex-row justify-between gap-8 items-center">
      <div>
        <h3 className="text-2xl font-bold mb-2">{company.name}</h3>
        <p className="text-gray-400">Professional Commercial Cleaning Services</p>
      </div>

      <div className="flex gap-4 flex-wrap">
        <a
          href={company.whatsapp}
          target="_blank"
          className="bg-green-500 px-5 py-3 rounded-xl font-semibold"
        >
          WhatsApp
        </a>

        <a
          href={`mailto:${company.email}`}
          className="bg-white text-black px-5 py-3 rounded-xl font-semibold"
        >
          Email
        </a>
      </div>
    </div>
  </footer>
</div>

); }
