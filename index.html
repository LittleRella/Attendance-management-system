import React, { useState } from 'react';
import { 
  Activity, BarChart3, BookOpen, Users, Grid3X3, QrCode, 
  Download, Upload, Edit3, Trash2, CheckCircle, 
  Smartphone, ShieldCheck, UserCheck,
  Calendar, Filter, FileSpreadsheet, Globe, ChevronRight,
  ArrowLeft, Mail, Phone, GraduationCap, MapPin
} from 'lucide-react';

const App = () => {
  // --- STATE ---
  const [activeView, setActiveView] = useState('overview');
  const [selectedStudent, setSelectedStudent] = useState(null); // For Profile Page
  const [editingStudent, setEditingStudent] = useState(null); // For Edit Modal
  const [attendanceMode, setAttendanceMode] = useState('physical');
  const [toast, setToast] = useState({ visible: false, message: '' });
  
  const [filters, setFilters] = useState({
    semester: 'Semester 1',
    year: '2024',
    month: 'January',
    date: new Date().toISOString().split('T')[0],
    cohort: 'MMBA 10',
    course: 'BUS701'
  });

  const [students, setStudents] = useState([
    { id: 's1', matric: '24/MMBA/001', fname: 'Sarah', lname: 'Ade', email: 'sarah.ade@edu.ng', phone: '+234 802 345 6789', cohort: 'MMBA 10', yield: 88, status: 'Active' },
    { id: 's2', matric: '24/EMBA/012', fname: 'John', lname: 'Doe', email: 'j.doe@corp.com', phone: '+234 810 123 4567', cohort: 'EMBA 31', yield: 72, status: 'Active' },
    { id: 's3', matric: '24/MEM/045', fname: 'Grace', lname: 'Eze', email: 'grace@edu.ng', phone: '+234 703 987 6543', cohort: 'MEMBA 13', yield: 95, status: 'Active' },
    { id: 's4', matric: '24/MMBA/002', fname: 'David', lname: 'Okon', email: 'david@gmail.com', phone: '+234 905 555 1234', cohort: 'MMBA 6', yield: 64, status: 'Warning' }
  ]);

  // --- CONFIGURATION DATA ---
  const generateRange = (prefix, start, end) => {
    const arr = [];
    for (let i = start; i <= end; i++) {
      arr.push(`${prefix} ${i}`);
    }
    return arr;
  };

  const ALL_COHORTS = [
    ...generateRange("MMBA", 6, 20),
    ...generateRange("MEMBA", 13, 20),
    ...generateRange("EMBA", 31, 40)
  ];

  const SEMESTERS = ["Semester 1", "Semester 2", "Summer"];
  const YEARS = ["2023", "2024", "2025"];
  
  const courses = [
    { id: 'c1', code: 'BUS701', name: 'Strategic Management' },
    { id: 'c2', code: 'FIN702', name: 'Corporate Finance' },
    { id: 'c3', code: 'MKT703', name: 'Digital Marketing' },
    { id: 'c4', code: 'OPS704', name: 'Operations Logic' }
  ];

  // --- ACTIONS ---
  const showToast = (msg) => {
    setToast({ visible: true, message: msg });
    setTimeout(() => setToast({ visible: false, message: '' }), 3000);
  };

  const downloadCSVTemplate = () => {
    const headers = "FirstName,LastName,MatricNo,Email,Phone,Cohort,CourseCode\n";
    const blob = new Blob([headers], { type: 'text/csv' });
    const url = window.URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.setAttribute('href', url);
    a.setAttribute('download', 'attendx_student_template.csv');
    a.click();
    showToast("Template downloaded successfully.");
  };

  const deleteStudent = (id) => {
    setStudents(students.filter(s => s.id !== id));
    showToast("Student record deleted.");
  };

  const saveEdit = (e) => {
    e.preventDefault();
    setStudents(students.map(s => s.id === editingStudent.id ? editingStudent : s));
    setEditingStudent(null);
    showToast("Student details updated.");
  };

  // --- RENDER LOGIC ---
  if (selectedStudent) {
    return <StudentProfilePage student={selectedStudent} onBack={() => setSelectedStudent(null)} />;
  }

  return (
    <div className="flex min-h-screen bg-[#f8fafc] text-slate-900 font-['Inter']">
      {/* Sidebar */}
      <aside className="w-[280px] bg-[#0b0f1a] text-white fixed h-full flex flex-col p-8 z-40">
        <div className="flex items-center gap-3 mb-12">
          <div className="bg-blue-600 p-2.5 rounded-xl shadow-lg shadow-blue-500/30">
            <Activity className="w-6 h-6" />
          </div>
          <h1 className="font-black text-2xl tracking-tighter uppercase italic text-white">AttendX</h1>
        </div>
        
        <nav className="space-y-1.5 flex-1">
          {[
            { id: 'overview', icon: <BarChart3 className="w-5 h-5" />, label: 'Dashboard' },
            { id: 'courses', icon: <BookOpen className="w-5 h-5" />, label: 'Manage Courses' },
            { id: 'registry', icon: <Users className="w-5 h-5" />, label: 'Student Registry' },
            { id: 'matrix', icon: <Grid3X3 className="w-5 h-5" />, label: 'Session Matrix' },
          ].map(item => (
            <button 
              key={item.id}
              onClick={() => setActiveView(item.id)}
              className={`w-full flex items-center gap-4 px-5 py-4 rounded-2xl transition-all font-bold text-sm text-left ${activeView === item.id ? 'bg-blue-600 text-white shadow-xl shadow-blue-500/20' : 'text-slate-400 hover:text-white/5'}`}
            >
              {item.icon} {item.label}
            </button>
          ))}
        </nav>

        <button 
          onClick={() => setActiveView('activate')}
          className={`w-full mt-auto py-5 rounded-2xl font-black text-sm tracking-wide flex items-center justify-center gap-3 transition-all ${activeView === 'activate' ? 'bg-blue-600 text-white shadow-xl shadow-blue-900/40' : 'bg-slate-800 text-slate-400'}`}
        >
          <QrCode className="w-5 h-5" /> GENERATE QR
        </button>
      </aside>

      {/* Main Content */}
      <main className="ml-[280px] flex-1 p-10 relative">
        <header className="flex justify-between items-start mb-6">
          <div>
            <h2 className="text-4xl font-black tracking-tighter text-slate-900 capitalize">{activeView.replace('-', ' ')}</h2>
            <p className="text-slate-500 font-medium text-sm mt-1">Enterprise management for MBA & Executive cohorts.</p>
          </div>
        </header>

        {/* Global Filters */}
        {(activeView === 'overview' || activeView === 'registry' || activeView === 'matrix') && (
          <div className="bg-white p-4 rounded-3xl shadow-sm border border-slate-100 flex flex-wrap gap-4 mb-10 items-center">
            <FilterSelect label="Cohort" value={filters.cohort} options={ALL_COHORTS} onChange={(v) => setFilters({...filters, cohort: v})} />
            <FilterSelect label="Course" value={filters.course} options={courses.map(c => c.code)} onChange={(v) => setFilters({...filters, course: v})} />
            <FilterSelect label="Semester" value={filters.semester} options={SEMESTERS} onChange={(v) => setFilters({...filters, semester: v})} />
            <FilterSelect label="Year" value={filters.year} options={YEARS} onChange={(v) => setFilters({...filters, year: v})} />
          </div>
        )}

        <div className="animate-in fade-in slide-in-from-bottom-4 duration-500">
          {activeView === 'overview' && <OverviewUI ALL_COHORTS={ALL_COHORTS} />}
          {activeView === 'courses' && <CourseUI courses={courses} />}
          {activeView === 'registry' && (
            <RegistryUI 
              students={students} 
              onDelete={deleteStudent} 
              onEdit={setEditingStudent}
              onViewProfile={setSelectedStudent}
              downloadCSVTemplate={downloadCSVTemplate}
            />
          )}
          {activeView === 'matrix' && <MatrixUI students={students} filters={filters} />}
          {activeView === 'activate' && (
            <ActivateUI 
              ALL_COHORTS={ALL_COHORTS} 
              courses={courses} 
              filters={filters} 
              setFilters={setFilters} 
              attendanceMode={attendanceMode} 
              setAttendanceMode={setAttendanceMode}
              showToast={showToast}
            />
          )}
        </div>

        {/* Edit Student Modal */}
        {editingStudent && (
          <div className="fixed inset-0 bg-slate-900/40 backdrop-blur-sm z-[60] flex items-center justify-center p-6">
            <div className="bg-white w-full max-w-lg rounded-[2.5rem] shadow-2xl p-10">
              <h3 className="text-2xl font-black mb-6">Edit Student Profile</h3>
              <form onSubmit={saveEdit} className="space-y-4">
                <div className="grid grid-cols-2 gap-4">
                  <Input label="First Name" value={editingStudent.fname} onChange={(v) => setEditingStudent({...editingStudent, fname: v})} />
                  <Input label="Last Name" value={editingStudent.lname} onChange={(v) => setEditingStudent({...editingStudent, lname: v})} />
                </div>
                <Input label="Matric Number" value={editingStudent.matric} onChange={(v) => setEditingStudent({...editingStudent, matric: v})} />
                <Input label="Email" value={editingStudent.email} onChange={(v) => setEditingStudent({...editingStudent, email: v})} />
                <div className="flex gap-4 pt-6">
                  <button type="button" onClick={() => setEditingStudent(null)} className="flex-1 bg-slate-100 text-slate-600 font-bold py-4 rounded-2xl">Cancel</button>
                  <button type="submit" className="flex-1 bg-blue-600 text-white font-bold py-4 rounded-2xl shadow-lg shadow-blue-500/20">Save Changes</button>
                </div>
              </form>
            </div>
          </div>
        )}
      </main>

      {/* Toast Notification */}
      {toast.visible && (
        <div className="fixed bottom-10 right-10 bg-slate-900 text-white px-8 py-5 rounded-2xl shadow-2xl flex items-center gap-4 z-[100] animate-in slide-in-from-right-4">
          <CheckCircle className="w-5 h-5 text-blue-400" />
          <span className="text-sm font-bold">{toast.message}</span>
        </div>
      )}
    </div>
  );
};

// --- SUB-COMPONENTS ---

const FilterSelect = ({ label, value, options, onChange }) => (
  <div className="flex flex-col min-w-[140px]">
    <span className="text-[9px] font-black text-slate-400 uppercase mb-1">{label}</span>
    <select 
      value={value} 
      onChange={(e) => onChange(e.target.value)}
      className="bg-slate-50 border-none rounded-xl text-xs font-bold px-3 py-2 outline-none cursor-pointer hover:bg-slate-100 transition-colors"
    >
      {options.map(opt => <option key={opt} value={opt}>{opt}</option>)}
    </select>
  </div>
);

const Input = ({ label, value, onChange }) => (
  <div>
    <label className="text-[10px] font-black text-slate-400 uppercase mb-1.5 block tracking-widest">{label}</label>
    <input 
      value={value} 
      onChange={(e) => onChange(e.target.value)}
      className="w-full bg-slate-50 border-none rounded-xl px-4 py-3 text-sm font-bold focus:ring-2 ring-blue-500/20 outline-none transition-all"
    />
  </div>
);

const PieChart = ({ percentage, color = "#2563eb" }) => {
  const radius = 18;
  const circumference = 2 * Math.PI * radius;
  const strokeDashoffset = circumference - (percentage / 100) * circumference;

  return (
    <div className="relative flex items-center justify-center w-16 h-16">
      <svg className="w-full h-full transform -rotate-90">
        <circle cx="32" cy="32" r={radius} stroke="currentColor" strokeWidth="4" fill="transparent" className="text-slate-100" />
        <circle
          cx="32" cy="32" r={radius} stroke={color} strokeWidth="4" fill="transparent"
          strokeDasharray={circumference} style={{ strokeDashoffset, transition: 'stroke-dashoffset 1.5s ease' }} strokeLinecap="round"
        />
      </svg>
      <span className="absolute text-[9px] font-black text-slate-900">{percentage}%</span>
    </div>
  );
};

const OverviewUI = ({ ALL_COHORTS }) => (
  <div className="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-6">
    {ALL_COHORTS.slice(0, 12).map((cohort, i) => {
      const percentage = Math.floor(Math.random() * 30) + 70;
      return (
        <div key={i} className="bg-white p-6 rounded-[2.5rem] shadow-sm border border-slate-100 flex items-center justify-between hover:shadow-xl hover:scale-[1.02] transition-all">
          <div>
            <h5 className="font-black text-slate-900 text-sm mb-1">{cohort}</h5>
            <p className="text-slate-400 text-[9px] font-bold uppercase tracking-wider italic">Engagement</p>
          </div>
          <PieChart percentage={percentage} />
        </div>
      );
    })}
  </div>
);

const CourseUI = ({ courses }) => (
  <div className="bg-white rounded-[3rem] p-10 shadow-sm border border-slate-100">
    <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
      {courses.map(c => (
        <div key={c.id} className="p-6 border border-slate-100 rounded-3xl flex justify-between items-center hover:bg-slate-50 transition-colors">
          <div>
            <div className="text-blue-600 font-black text-xs mb-1 uppercase tracking-widest">{c.code}</div>
            <div className="text-lg font-black text-slate-900">{c.name}</div>
          </div>
          <button className="p-2 text-slate-400 bg-white border border-slate-100 rounded-lg hover:text-blue-600"><Edit3 className="w-4 h-4" /></button>
        </div>
      ))}
    </div>
  </div>
);

const RegistryUI = ({ students, onDelete, onEdit, onViewProfile, downloadCSVTemplate }) => (
  <div className="bg-white rounded-[3rem] shadow-sm border border-slate-100 overflow-hidden">
    <div className="p-10 flex justify-between items-center bg-slate-50/30 border-b border-slate-100">
      <div>
        <h3 className="font-black text-2xl">Participant Roster</h3>
        <p className="text-[10px] text-slate-400 font-bold uppercase mt-1">Directory Management</p>
      </div>
      <div className="flex gap-3">
        <button onClick={downloadCSVTemplate} className="bg-white border border-slate-200 px-6 py-4 rounded-2xl text-xs font-black flex items-center gap-2 hover:bg-slate-50 transition-colors">
          <Download className="w-4 h-4" /> CSV TEMPLATE
        </button>
        <button className="bg-blue-600 text-white px-8 py-4 rounded-2xl text-xs font-black flex items-center gap-2 hover:bg-blue-700 shadow-lg shadow-blue-500/20">
          <Upload className="w-4 h-4" /> BULK UPLOAD
        </button>
      </div>
    </div>
    <table className="w-full text-left">
      <thead className="bg-slate-50 text-[10px] font-black text-slate-400 uppercase tracking-widest">
        <tr>
          <th className="px-10 py-6">Student Identity</th>
          <th className="px-10 py-6">Assigned Cohort</th>
          <th className="px-10 py-6">Participation Yield</th>
          <th className="px-10 py-6 text-right">Actions</th>
        </tr>
      </thead>
      <tbody className="divide-y divide-slate-50">
        {students.map(s => (
          <tr key={s.id} className="group hover:bg-slate-50/50 transition-colors">
            <td className="px-10 py-6">
              <button onClick={() => onViewProfile(s)} className="text-left">
                <div className="font-bold text-sm text-slate-900 group-hover:text-blue-600 transition-colors">{s.fname} {s.lname}</div>
                <div className="text-[10px] text-slate-400 font-mono tracking-tighter">{s.matric}</div>
              </button>
            </td>
            <td className="px-10 py-6">
              <span className="text-[10px] px-3 py-1 bg-slate-100 text-slate-600 font-black rounded-lg uppercase">{s.cohort}</span>
            </td>
            <td className="px-10 py-6">
              <div className="flex items-center gap-3">
                <div className="w-16 h-1.5 bg-slate-100 rounded-full overflow-hidden">
                  <div className="h-full bg-blue-600 rounded-full" style={{ width: `${s.yield}%` }}></div>
                </div>
                <span className="text-xs font-black">{s.yield}%</span>
              </div>
            </td>
            <td className="px-10 py-6 text-right">
              <div className="flex justify-end gap-2 opacity-0 group-hover:opacity-100 transition-opacity">
                <button onClick={() => onEdit(s)} className="p-2 text-slate-400 hover:text-blue-600 hover:bg-blue-50 rounded-lg transition-all"><Edit3 className="w-4 h-4" /></button>
                <button onClick={() => onDelete(s.id)} className="p-2 text-slate-400 hover:text-red-600 hover:bg-red-50 rounded-lg transition-all"><Trash2 className="w-4 h-4" /></button>
              </div>
            </td>
          </tr>
        ))}
      </tbody>
    </table>
  </div>
);

const StudentProfilePage = ({ student, onBack }) => (
  <div className="min-h-screen bg-[#f8fafc] p-10 animate-in fade-in slide-in-from-right-8 duration-500">
    <button onClick={onBack} className="flex items-center gap-2 text-slate-400 hover:text-slate-900 font-black text-xs uppercase mb-10 transition-colors">
      <ArrowLeft className="w-4 h-4" /> Back to Registry
    </button>
    
    <div className="grid grid-cols-1 lg:grid-cols-3 gap-10">
      <div className="lg:col-span-1 space-y-6">
        <div className="bg-white rounded-[3rem] p-10 shadow-sm border border-slate-100 text-center">
          <div className="w-24 h-24 bg-blue-600 rounded-[2rem] flex items-center justify-center text-white text-3xl font-black mx-auto mb-6 shadow-xl shadow-blue-500/20">
            {student.fname[0]}{student.lname[0]}
          </div>
          <h3 className="text-2xl font-black">{student.fname} {student.lname}</h3>
          <p className="text-slate-400 text-sm font-bold mt-1 italic tracking-tight">{student.matric}</p>
          <div className="mt-6 inline-flex items-center gap-2 px-4 py-2 bg-green-50 text-green-600 rounded-full text-[10px] font-black uppercase">
            <span className="w-2 h-2 bg-green-500 rounded-full"></span> {student.status}
          </div>
        </div>

        <div className="bg-white rounded-[2.5rem] p-8 shadow-sm border border-slate-100 space-y-6">
          <ProfileInfo icon={<Mail className="w-4 h-4" />} label="Email Address" value={student.email} />
          <ProfileInfo icon={<Phone className="w-4 h-4" />} label="Phone Number" value={student.phone} />
          <ProfileInfo icon={<GraduationCap className="w-4 h-4" />} label="Assigned Cohort" value={student.cohort} />
          <ProfileInfo icon={<MapPin className="w-4 h-4" />} label="Campus Access" value="Physical & Remote" />
        </div>
      </div>

      <div className="lg:col-span-2 space-y-10">
        <div className="grid grid-cols-2 gap-6">
          <div className="bg-white p-8 rounded-[2.5rem] shadow-sm border border-slate-100">
            <h4 className="text-[10px] font-black text-slate-400 uppercase mb-4 tracking-widest italic">Attendance Yield</h4>
            <div className="flex items-end gap-3">
              <span className="text-5xl font-black text-slate-900 leading-none">{student.yield}%</span>
              <div className="text-[10px] font-bold text-green-600 bg-green-50 px-2 py-1 rounded-md mb-1">+4.2% Monthly</div>
            </div>
          </div>
          <div className="bg-white p-8 rounded-[2.5rem] shadow-sm border border-slate-100">
            <h4 className="text-[10px] font-black text-slate-400 uppercase mb-4 tracking-widest italic">Module Progress</h4>
            <div className="flex items-end gap-3">
              <span className="text-5xl font-black text-slate-900 leading-none">08</span>
              <span className="text-slate-400 font-bold mb-1">/ 12 Courses</span>
            </div>
          </div>
        </div>

        <div className="bg-white rounded-[3rem] p-10 shadow-sm border border-slate-100">
          <h4 className="font-black text-xl mb-8">Recent Session Activity</h4>
          <div className="space-y-4">
            {[1, 2, 3].map(i => (
              <div key={i} className="flex items-center justify-between p-4 bg-slate-50 rounded-2xl border border-slate-100">
                <div className="flex gap-4">
                  <div className="w-10 h-10 bg-white rounded-xl flex items-center justify-center border border-slate-200">
                    <Calendar className="w-4 h-4 text-slate-400" />
                  </div>
                  <div>
                    <div className="font-bold text-sm">Strategic Management (BUS701)</div>
                    <div className="text-[10px] text-slate-400 font-black uppercase tracking-widest">Oct 12, 2024 • 09:00 AM</div>
                  </div>
                </div>
                <div className="flex items-center gap-2">
                   <div className="text-[10px] font-black uppercase bg-blue-100 text-blue-600 px-3 py-1 rounded-lg italic">Physical</div>
                   <CheckCircle className="w-5 h-5 text-green-500" />
                </div>
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  </div>
);

const ProfileInfo = ({ icon, label, value }) => (
  <div className="flex items-start gap-4">
    <div className="p-2 bg-slate-50 text-slate-400 rounded-lg">{icon}</div>
    <div>
      <p className="text-[9px] font-black text-slate-400 uppercase tracking-widest">{label}</p>
      <p className="text-sm font-bold text-slate-800">{value}</p>
    </div>
  </div>
);

const MatrixUI = ({ filters }) => (
  <div className="bg-white rounded-[3rem] shadow-sm border border-slate-100 overflow-hidden">
    <div className="p-10 bg-slate-50/30 border-b border-slate-100 flex justify-between items-center">
      <h3 className="font-black text-2xl">Session Engagement</h3>
      <div className="flex gap-2">
        <span className="px-3 py-1 bg-blue-600 text-white text-[10px] font-black rounded-lg">{filters.cohort}</span>
        <span className="px-3 py-1 bg-slate-900 text-white text-[10px] font-black rounded-lg">{filters.course}</span>
      </div>
    </div>
    <div className="p-20 text-center">
       <div className="bg-slate-50 border-2 border-dashed border-slate-200 rounded-[3rem] p-12">
          <Grid3X3 className="w-12 h-12 text-slate-200 mx-auto mb-4" />
          <p className="text-slate-400 font-bold italic text-sm">Attendance matrix for {filters.cohort} | {filters.course}</p>
          <button className="mt-6 bg-white border border-slate-200 px-6 py-3 rounded-xl text-[10px] font-black uppercase">Refresh Live Data</button>
       </div>
    </div>
  </div>
);

const ActivateUI = ({ ALL_COHORTS, courses, filters, setFilters, attendanceMode, setAttendanceMode, showToast }) => {
  const [studentChoice, setStudentChoice] = useState('physical');

  return (
    <div className="grid grid-cols-1 lg:grid-cols-2 gap-10">
      {/* Admin Control */}
      <div className="bg-white p-10 rounded-[3rem] shadow-sm border border-slate-100">
        <div className="flex items-center gap-3 mb-8">
          <div className="p-2 bg-blue-50 text-blue-600 rounded-lg"><QrCode className="w-5 h-5" /></div>
          <h3 className="text-2xl font-black uppercase tracking-tighter italic">Admin Controls</h3>
        </div>
        
        <div className="space-y-6">
          <FilterSelect label="Session Cohort" value={filters.cohort} options={ALL_COHORTS} onChange={(v) => setFilters({...filters, cohort: v})} />
          <FilterSelect label="Target Module" value={filters.course} options={courses.map(c => c.code)} onChange={(v) => setFilters({...filters, course: v})} />
          
          <div className="pt-4">
             <label className="text-[10px] font-black text-slate-400 uppercase mb-3 block tracking-widest text-center">Enforcement Mode</label>
             <div className="flex bg-slate-50 p-1.5 rounded-2xl">
               <button onClick={() => setAttendanceMode('physical')} className={`flex-1 py-3 rounded-xl font-black text-[10px] uppercase transition-all ${attendanceMode === 'physical' ? 'bg-white text-blue-600 shadow-sm' : 'text-slate-400 hover:text-slate-600'}`}>In-Person</button>
               <button onClick={() => setAttendanceMode('virtual')} className={`flex-1 py-3 rounded-xl font-black text-[10px] uppercase transition-all ${attendanceMode === 'virtual' ? 'bg-white text-indigo-600 shadow-sm' : 'text-slate-400 hover:text-slate-600'}`}>Virtual</button>
             </div>
          </div>

          <button onClick={() => showToast(`QR Session started for ${filters.cohort}`)} className="w-full bg-slate-900 text-white py-6 rounded-[2rem] font-black uppercase text-sm mt-4 shadow-xl shadow-slate-900/20 hover:bg-slate-800 transition-colors">
            Generate Dynamic Token
          </button>
        </div>
      </div>

      {/* Student Interface Preview */}
      <div className="flex flex-col items-center">
        <div className="flex items-center gap-2 mb-4 px-4">
          <Smartphone className="w-4 h-4 text-slate-400" />
          <span className="text-[10px] font-black text-slate-400 uppercase tracking-widest italic">Live Student Interface</span>
        </div>
        <div className="bg-slate-900 rounded-[3.5rem] p-4 shadow-2xl aspect-[9/18.5] w-[320px] border-[6px] border-slate-800 relative overflow-hidden ring-offset-4 ring-offset-[#f8fafc]">
          <div className="bg-white h-full rounded-[2.5rem] overflow-hidden flex flex-col">
            <div className="bg-blue-600 p-8 text-white text-center">
              <div className="bg-white/20 w-12 h-12 rounded-2xl flex items-center justify-center mx-auto mb-4 backdrop-blur-md">
                <ShieldCheck className="w-6 h-6" />
              </div>
              <h4 className="font-black text-lg tracking-tight leading-none uppercase italic">Verify Presence</h4>
              <p className="text-[9px] text-white/70 font-bold uppercase mt-1 tracking-widest">{filters.cohort} • {filters.course}</p>
            </div>

            <div className="p-6 flex-1 flex flex-col">
              <div className="bg-slate-50 p-4 rounded-2xl border border-slate-100 mb-6">
                <div className="flex items-center justify-between mb-3">
                  <span className="text-[9px] font-black text-slate-400 uppercase">Self-Select Mode</span>
                  <div className="bg-blue-100 text-blue-600 px-2 py-0.5 rounded text-[8px] font-black">REQUIRED</div>
                </div>
                
                <div className="grid grid-cols-2 gap-2">
                  <button onClick={() => setStudentChoice('physical')} className={`p-3 rounded-xl border text-[9px] font-black transition-all flex flex-col items-center gap-1 ${studentChoice === 'physical' ? 'bg-white border-blue-600 text-blue-600 shadow-sm ring-4 ring-blue-50' : 'bg-white border-slate-200 text-slate-400'}`}>
                    <UserCheck className="w-4 h-4" /> PHYSICAL
                  </button>
                  <button onClick={() => setStudentChoice('virtual')} className={`p-3 rounded-xl border text-[9px] font-black transition-all flex flex-col items-center gap-1 ${studentChoice === 'virtual' ? 'bg-white border-indigo-600 text-indigo-600 shadow-sm ring-4 ring-indigo-50' : 'bg-white border-slate-200 text-slate-400'}`}>
                    <Globe className="w-4 h-4" /> VIRTUAL
                  </button>
                </div>
              </div>

              <div className="flex-1 flex flex-col items-center justify-center border-2 border-dashed border-slate-100 rounded-[2rem] p-4 bg-slate-50/50 mb-6">
                 <QrCode className="w-20 h-20 text-slate-200" />
                 <p className="text-[8px] text-slate-400 font-bold uppercase mt-2">Ready for Token</p>
              </div>

              <button onClick={() => showToast("Presence Logged Successfully!")} className="w-full bg-slate-900 text-white py-4 rounded-2xl font-black text-[10px] uppercase flex items-center justify-center gap-2 group hover:bg-blue-600 transition-colors">
                Confirm Arrival <ChevronRight className="w-3 h-3 group-hover:translate-x-1 transition-transform" />
              </button>
            </div>
            <div className="h-1.5 w-1/3 bg-slate-100 mx-auto mb-4 rounded-full"></div>
          </div>
        </div>
      </div>
    </div>
  );
};

export default App;
